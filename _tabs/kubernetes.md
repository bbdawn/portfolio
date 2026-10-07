---
layout: page
title: Kubernetes
icon: fas fa-dharmachakra
order: 5
permalink: /kubernetes/
---

<style>
  #k8s * { box-sizing: border-box; }
  #k8s { margin: -0.5rem 0 0; }

  #k8s .gm-card {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 10px;
    padding: 1.25rem 1.4rem;
    margin-bottom: 1.25rem;
    background: var(--card-bg, rgba(0,0,0,0.015));
  }
  #k8s .gm-card h3 {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 0.6rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  #k8s .gm-card h3 i { color: var(--link-color); opacity: 0.85; }
  #k8s .gm-card p { font-size: 0.92rem; line-height: 1.75; opacity: 0.85; }
  #k8s .gm-card ul { font-size: 0.92rem; line-height: 1.8; opacity: 0.85; padding-left: 1.2rem; }

  #k8s .gm-note {
    font-size: 0.85rem;
    line-height: 1.8;
    padding: 0.7rem 1rem;
    border-left: 3px solid var(--link-color);
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.06);
    border-radius: 4px;
    margin: 0.75rem 0;
  }
  #k8s .gm-note.warn { border-left-color: #dc3545; background: rgba(220,53,69,0.06); }

  #k8s pre { overflow-x: auto; font-size: 0.8rem; line-height: 1.55; background: var(--code-bg, #f6f6f6); border: 1px solid var(--border-color, #dee2e6); border-radius: 8px; padding: 0.8rem 1rem; margin: 0.6rem 0 0.9rem; }

  #k8s table.gm-table {
    width: 100%;
    font-size: 0.86rem;
    border-collapse: collapse;
    margin: 0.75rem 0 0.25rem;
  }
  #k8s table.gm-table th,
  #k8s table.gm-table td {
    border: 1px solid var(--border-color, #dee2e6);
    padding: 0.5rem 0.7rem;
    text-align: left;
    vertical-align: top;
    white-space: normal;
    word-break: keep-all;
  }
  #k8s table.gm-table th { background: rgba(0,0,0,0.03); }
  #k8s .gm-table-wrap { overflow-x: auto; }

  #k8s .gm-compare-badge {
    display: inline-block; font-size: 0.72rem; font-weight: 700;
    border-radius: 4px; padding: 0.1rem 0.5rem; margin-right: 0.4rem;
  }
  #k8s .gm-compare-badge.before { background: rgba(220,53,69,0.12); color: #dc3545; }
  #k8s .gm-compare-badge.after { background: rgba(40,167,69,0.12); color: #28a745; }
  #k8s .gm-compare-badge.dev { background: rgba(var(--bs-primary-rgb, 13,110,253), 0.12); color: var(--link-color); }

  #k8s .gm-github-btn {
    display: inline-flex; align-items: center; gap: 0.5rem;
    background: #24292f; color: #fff !important;
    border-radius: 8px; padding: 0.6rem 1.1rem;
    font-size: 0.92rem; font-weight: 600;
    text-decoration: none !important;
    margin: 0.25rem 0 0.5rem;
  }
  #k8s .gm-github-btn:hover { background: #000; }

  #k8s .gm-feature-shot {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px;
    padding: 0.75rem;
    margin: 0.75rem 0 1rem;
    background: var(--code-bg, #f6f6f6);
  }
  #k8s .gm-feature-shot img { max-width: 100%; height: auto; border-radius: 6px; display: block; margin: 0 auto; }
  #k8s .gm-shot-caption { font-size: 0.8rem; opacity: 0.65; margin-top: 0.35rem; text-align: center; }
  #k8s .gm-feature-shot.gm-shot-multi { display: flex; flex-direction: column; gap: 1rem; }
  #k8s .gm-shot-step { font-size: 0.72rem; font-weight: 700; color: var(--link-color); letter-spacing: 0.06em; margin-bottom: 0.35rem; }

  /* 프로젝트 구분 */
  #k8s .k8s-project {
    display: flex; align-items: center; gap: 0.6rem;
    margin: 2.25rem 0 1rem; padding-bottom: 0.5rem;
    border-bottom: 2px solid var(--link-color);
  }
  #k8s .k8s-project:first-child { margin-top: 0.25rem; }
  #k8s .k8s-project-num {
    font-size: 0.72rem; font-weight: 800; letter-spacing: 0.08em;
    color: #fff; background: var(--link-color); border-radius: 4px; padding: 0.15rem 0.5rem;
  }
  #k8s .k8s-project-title { font-size: 1.2rem; font-weight: 800; letter-spacing: -0.01em; }
  #k8s .k8s-personal { margin-left: auto; font-size: 0.72rem; font-weight: 700; color: #28a745; background: rgba(40,167,69,0.12); border-radius: 4px; padding: 0.15rem 0.5rem; white-space: nowrap; }

  /* 3칸 박스 */
  #k8s .gs-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 0.6rem; margin: 0.9rem 0 0.25rem; }
  #k8s .gs-box {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px; padding: 0.8rem 0.9rem; background: var(--main-bg, #fff);
  }
  #k8s .gs-box-label { font-size: 0.7rem; font-weight: 700; opacity: 0.5; text-transform: uppercase; letter-spacing: 0.06em; }
  #k8s .gs-box-value { font-size: 0.92rem; font-weight: 700; margin-top: 0.15rem; line-height: 1.45; }

  @media (max-width: 768px) {
    #k8s .gs-grid { grid-template-columns: repeat(2, 1fr); }
  }
</style>

<div id="k8s">

  <!-- ═════════════════════ 프로젝트 1 ═════════════════════ -->
  <div class="k8s-project">
    <span class="k8s-project-num">PROJECT 1</span>
    <span class="k8s-project-title">OpenStack 위 Kubernetes 클러스터 구축</span>
    <span class="k8s-personal">개인 프로젝트</span>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-lightbulb"></i> 개요</h3>
    <p>OpenStack에 VM 3대를 생성하고 kubeadm으로 Kubernetes 클러스터(Control Plane 1대 + Worker 2대)를 직접 구성했습니다.<br>
    nginx를 Deployment로 배포해 NodePort로 외부에 노출하고, Pod 삭제·노드 장애 상황에서 Kubernetes가 원하는 상태를 어떻게 유지하는지 검증했습니다.</p>
    <div class="gs-grid">
      <div class="gs-box"><div class="gs-box-label">OS</div><div class="gs-box-value">Ubuntu 24.04</div></div>
      <div class="gs-box"><div class="gs-box-label">Runtime</div><div class="gs-box-value">containerd 2.2.1</div></div>
      <div class="gs-box"><div class="gs-box-label">Kubernetes</div><div class="gs-box-value">kubeadm 1.34.11</div></div>
      <div class="gs-box"><div class="gs-box-label">CNI</div><div class="gs-box-value">Calico 3.30.3</div></div>
    </div>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-server"></i> 클러스터 구성</h3>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>VM</th><th>역할</th><th>CPU</th><th>RAM</th><th>Disk</th></tr>
        <tr><td><code>k8s-cp</code></td><td>Control Plane (API Server, Scheduler, Controller Manager, etcd)</td><td>2 Core</td><td>4GB</td><td>30GB</td></tr>
        <tr><td><code>k8s-worker1</code></td><td>Worker (애플리케이션 Pod 실행)</td><td>2 Core</td><td>4GB</td><td>30GB</td></tr>
        <tr><td><code>k8s-worker2</code></td><td>Worker (애플리케이션 Pod 실행)</td><td>2 Core</td><td>4GB</td><td>30GB</td></tr>
      </table>
    </div>
    <p style="margin-top:0.9rem;"><strong>구축 순서</strong></p>
<pre><code>hostname · /etc/hosts  →  swap off  →  커널 모듈(overlay, br_netfilter) · ip_forward
        ↓
containerd 설치 (SystemdCgroup = true)
        ↓
kubeadm / kubelet / kubectl 설치
        ↓
kubeadm init (k8s-cp)  →  kubeadm join (worker1, worker2)
        ↓
Calico CNI 설치  →  3개 노드 모두 Ready</code></pre>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-rocket"></i> 서비스 배포</h3>
    <p>nginx를 Deployment로 배포하고 NodePort Service로 노출해, 클러스터 밖에서 노드 IP:NodePort로 접속되는 것을 확인했습니다. Pod IP(192.168.x.x, Calico)는 VM 네트워크와 다른 대역이라, 외부 접근은 Service를 통해 이루어집니다.</p>
<pre><code>외부  ──:30933──▶  Node (NodePort)  ──▶  Service nginx (ClusterIP :80)  ──▶  nginx Pod ×3
                                                                 (worker1, worker2에 분산)</code></pre>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/k8s-cluster-nginx-nodeport.png" alt="브라우저에서 NodePort로 nginx 접속">
      <div class="gm-shot-caption">브라우저에서 노드 IP:NodePort로 접속한 nginx 화면</div>
    </div>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-heartbeat"></i> 장애 시나리오 검증</h3>
    <p>replicas를 3으로 늘린 뒤, Pod와 노드에 장애 상황을 만들어 Kubernetes의 동작을 확인했습니다.</p>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>시나리오</th><th>조작</th><th>결과</th></tr>
        <tr><td>Pod 장애</td><td><code>kubectl delete pod</code></td><td>ReplicaSet이 차이를 감지해 새 Pod를 생성, 3개 유지 (self-healing)</td></tr>
        <tr><td>노드 스케줄링 금지</td><td><code>kubectl cordon k8s-worker1</code> 후 Pod 삭제</td><td>새 Pod가 worker1이 아닌 worker2에 배치</td></tr>
        <tr><td>노드 비우기</td><td><code>kubectl drain k8s-worker1</code></td><td>worker1의 기존 Pod까지 축출되어 worker2에 재생성</td></tr>
        <tr><td>노드 복귀</td><td><code>kubectl uncordon k8s-worker1</code></td><td>worker1이 다시 스케줄링 대상으로 복귀</td></tr>
      </table>
    </div>
    <div class="gm-note">
      <strong>확인한 것</strong> — Pod는 "이동"하지 않습니다. 기존 Pod가 삭제되고 ReplicaSet이 새 Pod를 만들기 때문에 이름과 IP가 바뀌며, Service가 살아 있는 Pod를 자동으로 다시 찾아 연결합니다.
    </div>
  </div>

  <!-- ═════════════════════ 프로젝트 2 ═════════════════════ -->
  <div class="k8s-project">
    <span class="k8s-project-num">PROJECT 2</span>
    <span class="k8s-project-title">영수증 OCR 워크로드 배포</span>
    <span class="k8s-personal">개인 프로젝트</span>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-question-circle"></i> 왜 만들었는가</h3>
    <p>회사에서 법인카드 사용 내역을 청구할 때는 영수증 파일명을 정해진 형식(날짜·가맹점·용도·매장)으로 바꿔서 첨부해야 했습니다. 많게는 한 달에 40장의 영수증을 하나씩 열어 결제일시와 가맹점, 결제 시각을 확인하고 파일명을 직접 바꿔야 했습니다.</p>
    <p>매달 반복되는 이 작업을 없애기 위해, 영수증을 올리기만 하면 파일명이 자동으로 만들어지는 OCR 서비스를 만들었습니다.</p>
    <div class="gm-note">
      <span class="gm-compare-badge before">BEFORE</span>영수증마다 열어서 정보 확인 → 파일명 직접 입력 (개인별 월 40장)<br>
      <span class="gm-compare-badge after">AFTER</span>여러 장을 한 번에 업로드 → 파일명 자동 생성 → 바뀐 이름으로 바로 다운로드해 청구에 첨부
    </div>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-lightbulb"></i> 개요</h3>
    <p>영수증 이미지를 올리면 OCR로 결제 정보를 읽어 청구용 파일명을 자동으로 만들어 주는 서비스입니다.<br>
    FastAPI와 PaddleOCR로 만들고, 위에서 직접 구축한 Kubernetes 클러스터에 배포했습니다. 이후 Pod 개수에 따른 성능 측정에도 활용할 수 있도록 추론 시간을 따로 측정하는 구조로 설계했습니다.</p>
    <a class="gm-github-btn" href="https://github.com/bbdawn/k8s-platform" target="_blank" rel="noopener">
      <i class="fab fa-github"></i> GitHub에서 k8s-platform 보기
    </a>
    <div class="gs-grid">
      <div class="gs-box"><div class="gs-box-label">API</div><div class="gs-box-value">FastAPI</div></div>
      <div class="gs-box"><div class="gs-box-label">OCR</div><div class="gs-box-value">PaddleOCR 3.7</div></div>
      <div class="gs-box"><div class="gs-box-label">Build</div><div class="gs-box-value">buildkit</div></div>
      <div class="gs-box"><div class="gs-box-label">Deploy</div><div class="gs-box-value">Kustomize · NodePort</div></div>
    </div>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-receipt"></i> 영수증 파일명 자동 생성</h3>
    <p>영수증 이미지를 올리면 OCR 결과에서 필요한 값을 뽑아 경비 처리용 파일명을 만들어 줍니다. 여러 장을 한 번에 올려 전체 복사·다운로드할 수 있습니다.</p>
<pre><code>26.08.05(주)우아한형제들_점심_메머드
   │          │          │     └ 판매자 정보 &gt; 상호 (첫 단어, 실제 매장)
   │          │          └ 결제 시각 17시 이후면 저녁, 이전이면 점심
   │          └ 가맹점 정보 &gt; 상호 (결제 주체)
   └ 결제일시 → YY.MM.DD</code></pre>
    <div class="gm-feature-shot gm-shot-multi">
      <div>
        <div class="gm-shot-step">STEP 1 · 업로드</div>
        <img src="/assets/img/posts/ocr-upload-empty.png" alt="영수증 OCR 업로드 화면">
        <div class="gm-shot-caption">영수증 이미지를 끌어다 놓거나 선택해서 업로드 (여러 장 동시 선택 가능)</div>
      </div>
      <div>
        <div class="gm-shot-step">STEP 2 · 인식</div>
        <img src="/assets/img/posts/ocr-upload-processing.png" alt="여러 장의 영수증을 동시에 인식하는 화면">
        <div class="gm-shot-caption">여러 장의 영수증을 한 번에 올려 인식</div>
      </div>
      <div>
        <div class="gm-shot-step">STEP 3 · 파일명 생성</div>
        <img src="/assets/img/posts/ocr-upload-result.png" alt="인식 결과와 생성된 파일명">
        <div class="gm-shot-caption">결제일시·가맹점·용도·판매자를 추출해 <code>26.09.14(주)우아한형제들_점심_싱싱샐러드</code> 형식의 파일명을 생성하고, 복사하거나 그 이름으로 바로 다운로드</div>
      </div>
    </div>
    <ul>
      <li><strong>생성된 파일명으로 원본 이미지를 바로 다운로드</strong> — 이름을 따로 바꿀 필요 없이 받은 파일을 그대로 청구에 첨부 (여러 장은 전체 다운로드)</li>
      <li>배달앱처럼 결제 주체(가맹점)와 실제 매장(판매자)이 다른 영수증을 고려해 두 섹션을 구분해 추출</li>
      <li>OCR이 공백을 지워 붙인 날짜·시각을 파싱하고, 사업자번호를 날짜로 오인하지 않도록 유효한 날짜만 채택</li>
      <li>추출은 휴리스틱이라 틀릴 수 있으므로 네 항목 모두 화면에서 수정 가능</li>
    </ul>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-cubes"></i> 배포 구성</h3>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>리소스</th><th>내용</th></tr>
        <tr><td>Namespace</td><td><code>ocr-bench</code></td></tr>
        <tr><td>ConfigMap</td><td>OCR 언어, 동시성, 이미지 크기 제한, 스레드 수 등 모든 설정을 환경변수로 분리</td></tr>
        <tr><td>Deployment</td><td>replicas 1, <code>strategy: Recreate</code>, CPU 1500m · 메모리 3Gi (requests = limits, Guaranteed QoS)</td></tr>
        <tr><td>Probe</td><td>startup·readiness는 <code>/ready</code>(OCR 엔진 상태), liveness는 <code>/health</code></td></tr>
        <tr><td>Service</td><td>NodePort 30800</td></tr>
        <tr><td>노드 배치</td><td><code>ocr-bench/role=target</code> 라벨로 측정 대상 노드 고정. worker1은 OCR, worker2는 부하 생성 도구용으로 분리</td></tr>
      </table>
    </div>
    <p style="margin-top:0.75rem;">amd64인 Worker 노드에서 buildkit으로 직접 이미지를 빌드해 containerd의 <code>k8s.io</code> 네임스페이스에 넣는 방식으로 배포했습니다. OCR 모델은 빌드 단계에서 이미지에 구워, 모델 다운로드 시간이 Pod 기동 시간에 섞이지 않게 했습니다.</p>
  </div>

</div>
