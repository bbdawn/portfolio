---
layout: page
title: Private Cloud
icon: fas fa-cloud
order: 1
permalink: /private-cloud/
---

<style>
  #pc * { box-sizing: border-box; }
  #pc { margin: -0.5rem 0 0; }

  #pc .gm-card {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 10px;
    padding: 1.25rem 1.4rem;
    margin-bottom: 1.25rem;
    background: var(--card-bg, rgba(0,0,0,0.015));
  }
  #pc .gm-card h3 {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 0.6rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  #pc .gm-card h3 i { color: var(--link-color); opacity: 0.85; }
  #pc .gm-card p { font-size: 0.92rem; line-height: 1.75; opacity: 0.85; }
  #pc .gm-card ul { font-size: 0.92rem; line-height: 1.8; opacity: 0.85; padding-left: 1.2rem; }

  #pc .gm-note {
    font-size: 0.85rem;
    line-height: 1.8;
    padding: 0.7rem 1rem;
    border-left: 3px solid var(--link-color);
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.06);
    border-radius: 4px;
    margin: 0.75rem 0;
  }

  #pc pre {
    overflow-x: auto; font-size: 0.8rem; line-height: 1.55;
    background: var(--code-bg, #f6f6f6); border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px; padding: 0.8rem 1rem; margin: 0.6rem 0 0.9rem;
  }

  #pc table.gm-table {
    width: 100%;
    font-size: 0.86rem;
    border-collapse: collapse;
    margin: 0.75rem 0 0.25rem;
  }
  #pc table.gm-table th,
  #pc table.gm-table td {
    border: 1px solid var(--border-color, #dee2e6);
    padding: 0.5rem 0.7rem;
    text-align: left;
    vertical-align: top;
    white-space: normal;
    word-break: keep-all;
  }
  #pc table.gm-table th { background: rgba(0,0,0,0.03); }
  #pc .gm-table-wrap { overflow-x: auto; }

  #pc .gm-compare-badge {
    display: inline-block; font-size: 0.72rem; font-weight: 700;
    border-radius: 4px; padding: 0.1rem 0.5rem; margin-right: 0.4rem;
  }
  #pc .gm-compare-badge.before { background: rgba(220,53,69,0.12); color: #dc3545; }
  #pc .gm-compare-badge.after { background: rgba(40,167,69,0.12); color: #28a745; }

  #pc .gm-github-btn {
    display: inline-flex; align-items: center; gap: 0.5rem;
    background: #24292f; color: #fff !important;
    border-radius: 8px; padding: 0.6rem 1.1rem;
    font-size: 0.92rem; font-weight: 600;
    text-decoration: none !important;
    margin: 0.25rem 0 0.5rem;
  }
  #pc .gm-github-btn:hover { background: #000; }

  #pc .gm-feature-shot {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px;
    padding: 0.75rem;
    margin: 0.75rem 0 1rem;
    background: var(--code-bg, #f6f6f6);
  }
  #pc .gm-feature-shot img { max-width: 100%; height: auto; border-radius: 6px; display: block; margin: 0 auto; }
  #pc .gm-shot-caption { font-size: 0.8rem; opacity: 0.65; margin-top: 0.35rem; text-align: center; }

  #pc .pc-sub { font-size: 0.95rem; font-weight: 700; margin: 1.1rem 0 0.4rem; }
  #pc .pc-sub:first-of-type { margin-top: 0.25rem; }
</style>

<div id="pc">

  <!-- ══════════ 개요 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-lightbulb"></i> 개요</h3>
    <p><a href="https://www.okestro.com/solution/contrabass/" target="_blank" rel="noopener">콘트라베이스(Contrabass)</a>는 OpenStack 기반 Private Cloud IaaS 자원 관리 포탈입니다.<br>사용자는 CLI 없이 포탈 화면에서 Compute, Network, Storage, Load Balancer 자원을 생성하고 관리할 수 있습니다.<br>
    이 포탈의 백엔드에서 OpenStack 각 서비스와 연동되는 자원 관리 기능을 개발하고 운영했습니다.</p>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>자원</th><th>OpenStack</th><th>개발한 기능</th></tr>
        <tr><td>Network</td><td>Neutron</td><td>Floating IP 연동 가능 여부 표출, 포트 기준 보안그룹 조회 API</td></tr>
        <tr><td>Load Balancer</td><td>Octavia · Barbican</td><td>TERMINATED_HTTPS SSL Offloading, .p12 인증서 업로드</td></tr>
        <tr><td>Storage</td><td>Cinder</td><td>볼륨 그룹(Volume Group) 관리</td></tr>
        <tr><td>Compute</td><td>Nova · Placement</td><td>GPU Instance, GPU 인벤토리 관리 (<a href="{{ '/gpu/' | relative_url }}">GPU</a> 참고)</td></tr>
      </table>
    </div>
  </div>

  <!-- ══════════ RFP 검토 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-clipboard-check"></i> RFP 요구사항 기술 검토</h3>
    <p>RFP의 <strong>GPU, Network, Load Balancer, VM Lifecycle 관리</strong> 요구사항을 콘트라베이스에 구현된 기능과 하나씩 대조해 충족 가능 여부를 검토하고, 기술적인 의견을 전달했습니다.</p>
<pre><code>RFP 요구사항  →  구현된 기능과 대조  →  충족 가능 여부 판단  →  기술 의견 전달
                                      (충족 / 부분 충족 / 미충족)</code></pre>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>검토 영역</th><th>검토 관점</th></tr>
        <tr><td>GPU</td><td>요구하는 GPU 할당 방식과 지원 범위를 현재 구현과 비교</td></tr>
        <tr><td>Network</td><td>네트워크 서비스, IP 관리 요구사항의 제공 범위 확인</td></tr>
        <tr><td>Load Balancer</td><td>로드밸런서 및 연계 기능의 동작 조건 확인</td></tr>
        <tr><td>VM Lifecycle</td><td>VM 생성·삭제·전원 관리, 스냅샷 등 라이프사이클 기능 충족 여부 확인</td></tr>
      </table>
    </div>
    <div class="gm-note">부분적으로 충족하는 항목은 <strong>어떤 조건에서 충족되는지</strong> 기술적 근거를 함께 정리해, 사업팀이 수용 방안과 검수 기준을 정할 수 있도록 했습니다.</div>
  </div>

  <!-- ══════════ Floating IP ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-user-check"></i> 사용자 경험 개선 — Floating IP 연동 가능 여부 표출</h3>
    <p><span class="gm-compare-badge before">BEFORE</span>Floating IP는 라우터가 연결되지 않은 네트워크의 포트와는 연동할 수 없습니다. 기존 화면은 포트 목록을 그대로 보여줬기 때문에, 사용자가 연동할 수 없는 포트를 골라 오류를 만나는 상황이 반복됐습니다.</p>
    <p class="pc-sub">연동 가능 조건</p>
<pre><code>[External Network]
       ↕  External Gateway   ← 라우터에 External Gateway가 설정되어 있는가
   [Router]
       ↕  Router Interface   ← 포트의 네트워크에 라우터 인터페이스가 있는가
   [Network]
       ↕
    [Port]  ← Floating IP 연동 대상 (Internal Network 포트만 가능)</code></pre>
    <p>External Gateway가 설정된 라우터와 그 인터페이스가 속한 네트워크를 모아 "라우팅 가능한 네트워크"를 구하고, 포트 목록을 내려줄 때 각 포트의 연동 가능 여부를 함께 반환하도록 구현했습니다.</p>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/floating-ip-connectivity-associate-dialog.png" alt="유동 IP 자원 연동 화면 - 연동 가능 여부 표출">
      <div class="gm-shot-caption">유동 IP 자원 연동 화면에서 고정 IP별 연동 가능 여부와 불가 사유를 표시</div>
    </div>
    <p><span class="gm-compare-badge after">AFTER</span>사용자는 연동 가능한 포트를 화면에서 바로 구분할 수 있고, 연동할 수 없는 경우 그 이유를 함께 확인합니다.</p>
    <ul>
      <li>연동 불가 포트를 선택했을 때 발생하던 오류를 사전에 차단</li>
      <li>Neutron API 호출 실패로 인한 불필요한 에러 로그 감소</li>
    </ul>
  </div>

  <!-- ══════════ SSL Offloading ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-lock"></i> Octavia SSL Offloading</h3>
    <p>Octavia 로드밸런서의 Listener를 <code>TERMINATED_HTTPS</code>로 생성하면, 클라이언트와의 TLS를 로드밸런서에서 종료하고 백엔드 서버로는 HTTP로 전달합니다. 인증서는 OpenStack Barbican에 저장하고 Octavia가 이를 참조합니다.</p>
<pre><code>[클라이언트]  ── HTTPS (TLS) ──▶  [Octavia Load Balancer]  ── HTTP ──▶  [백엔드 서버]
                                   ↑ Barbican 인증서 적용</code></pre>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/octavia-ssl-offloading-listener-create.png" alt="로드밸런서 리스너 생성 화면 - TERMINATED_HTTPS 프로토콜 및 SSL 인증서 선택">
      <div class="gm-shot-caption">리스너 생성 화면에서 TERMINATED_HTTPS 선택 시 SSL 인증서 목록이 노출되는 모습</div>
    </div>

    <p class="pc-sub">사용자 친화적인 인증서 등록</p>
    <p><span class="gm-compare-badge before">BEFORE</span>Barbican에 인증서를 등록하려면 <code>.p12</code> 파일을 직접 base64로 인코딩해 입력해야 했습니다. 번거롭고 실수가 생기기 쉬운 과정이었습니다.</p>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/octavia-ssl-offloading-cert-manual-input.png" alt="SSL 인증서 등록 화면 - Payload 데이터 직접 입력">
      <div class="gm-shot-caption">기존 방식: base64로 인코딩한 Payload를 직접 입력</div>
    </div>
    <p><span class="gm-compare-badge after">AFTER</span>포탈에서 <code>.p12</code> 파일을 그대로 올리면 백엔드가 base64 변환과 Barbican 등록까지 처리합니다.</p>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/octavia-ssl-offloading-cert-p12-upload.png" alt="SSL 인증서 등록 화면 - pkcs#12 파일 업로드">
      <div class="gm-shot-caption">개선된 방식: .p12 파일 업로드만으로 인증서 등록</div>
    </div>
  </div>

  <!-- ══════════ 보안그룹 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-shield-alt"></i> 포트 기준 보안그룹 조회 API</h3>
    <p>보안그룹은 인스턴스가 아니라 인스턴스에 연결된 <strong>포트</strong>에 적용됩니다. 포트 하나에 여러 보안그룹이 적용될 수 있고, 보안그룹이 없는 포트도 있습니다.</p>
<pre><code>Instance
 ├── Port1 ── SG-A, SG-B
 ├── Port2 ── SG-B
 └── Port3 ── (보안그룹 없음)</code></pre>
    <p>Nova API는 인스턴스의 보안그룹을 포트 구분 없이 중복값을 포함해 반환해서, 같은 보안그룹이 화면에 여러 번 보이는 문제가 있었습니다. 이를 해결하기 위해 <strong>포트 단위로 보안그룹을 구분해 반환하는 API</strong>를 개발했습니다.</p>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/openstack-security-group-instance-detail.png" alt="인스턴스 상세 화면 - 포트별 보안그룹 목록">
      <div class="gm-shot-caption">인스턴스 상세 화면에서 포트별로 적용된 보안그룹을 구분해 표시</div>
    </div>
  </div>

  <!-- ══════════ 볼륨 그룹 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-hdd"></i> Cinder 볼륨 그룹 관리</h3>
    <p>여러 볼륨이 함께 있어야 의미가 있는 작업(그룹 단위 스냅샷, 백업)에서는 볼륨 간 정합성이 중요합니다. Cinder의 Volume Group으로 여러 볼륨을 묶어 <strong>같은 시점 기준</strong>으로 다룰 수 있도록, 콘트라베이스에서 볼륨 그룹을 관리하는 기능을 개발했습니다.</p>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>기능</th><th>설명</th></tr>
        <tr><td>그룹 생성</td><td>Volume Group Type 지정 후 그룹 생성</td></tr>
        <tr><td>볼륨 추가/제거</td><td>기존 볼륨을 그룹에 편입하거나 그룹에서 제외</td></tr>
        <tr><td>그룹 조회</td><td>그룹에 속한 볼륨 목록 및 상태 조회</td></tr>
        <tr><td>그룹 삭제</td><td>그룹 및 그룹 내 볼륨 처리 옵션 포함 삭제</td></tr>
      </table>
    </div>
    <div class="gm-note">이 기능은 이후 인스턴스에 연결된 여러 볼륨을 같은 시점으로 복제해야 하는 <strong>인스턴스 복제</strong> 기능의 기반 자원으로 사용되었습니다. (인스턴스 복제 구현은 다른 팀원이 진행)</div>
  </div>

  <!-- ══════════ 자동화 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-robot"></i> 운영 자동화 — Load Balancer Pool Member 자동 구축</h3>
    <p>로드밸런서 동작을 확인하려면 Pool Member VM을 만들고 웹 서버를 설치하는 작업을 매번 반복해야 했습니다. Terraform과 Ansible로 이 과정을 자동화해, <code>terraform apply</code> 한 번으로 테스트 환경이 구성되게 만들었습니다.</p>
<pre><code>terraform apply
   → OpenStack에 pool-member-1, pool-member-2 VM 생성
   → VM IP로 Ansible inventory 자동 생성
   → ansible-playbook 자동 실행 (nginx 설치 + VM별 다른 페이지 배포)</code></pre>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>항목</th><th>이전 (수동)</th><th>이후 (Terraform + Ansible)</th></tr>
        <tr><td>VM 생성</td><td>대시보드에서 VM 2대 직접 생성</td><td><code>terraform apply</code> 한 번</td></tr>
        <tr><td>Ansible inventory</td><td>IP 확인 후 수동 작성</td><td>자동 생성</td></tr>
        <tr><td>nginx 설치 + 페이지 배포</td><td>VM마다 SSH 접속 후 수동 설정</td><td>apply 시 자동 실행</td></tr>
        <tr><td>Pool Member 구분</td><td>접속해서 직접 확인</td><td>VM별 페이지 색상으로 즉시 구분</td></tr>
      </table>
    </div>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/pool-member-nginx-pages.png" alt="pool-member-1(Blue), pool-member-2(Red) 결과 화면">
      <div class="gm-shot-caption">VM마다 다른 색상의 페이지를 배포해, 로드밸런서의 트래픽 분배를 브라우저에서 바로 확인</div>
    </div>
    <a class="gm-github-btn" href="https://github.com/bbdawn/terraform-ansible-lab" target="_blank" rel="noopener">
      <i class="fab fa-github"></i> GitHub에서 terraform-ansible-lab 보기
    </a>
  </div>

  <!-- ══════════ 장애 대응 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-wrench"></i> 운영 장애 대응 — Load Balancer 생성 실패</h3>
    <div class="gm-table-wrap">
      <table class="gm-table">
        <tr><th>증상</th><th>원인</th><th>해결</th></tr>
        <tr><td><code>Anti-affinity instance group policy was violated</code></td><td>Amphora 서버 그룹의 anti-affinity 정책상, 그룹 내 VM 수가 사용 가능한 Compute 호스트 수보다 많음</td><td>호스트 추가, 불필요한 VM 정리, 또는 환경에 맞게 soft-anti-affinity 적용</td></tr>
        <tr><td>노드 재부팅 후 Load Balancer 생성 실패</td><td>Health Manager와 Amphora가 통신하는 <code>o-hm0</code> 인터페이스가 사라짐</td><td>Neutron의 Health Manager 포트 정보(MAC, port id)로 OVS <code>br-int</code>에 인터페이스 재생성</td></tr>
      </table>
    </div>
  </div>

  <!-- ══════════ 서비스 구성 예시 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-project-diagram"></i> 포탈로 서비스 환경 구성하기</h3>
    <p>콘트라베이스 화면만으로 하나의 서비스 환경을 처음부터 끝까지 구성할 수 있습니다. 네트워크부터 공유 볼륨까지, Neutron · Nova · Octavia · Manila를 어떤 순서로 엮어 쓰는지 직접 구성해 확인했습니다.</p>
<pre><code>외부/내부 네트워크 생성 (Neutron)  →  인스턴스 생성 (Nova)  →  유동 IP 생성
        ↓
라우터로 외부/내부 네트워크 연결  →  VM에 유동 IP 연동
        ↓
로드밸런서 생성 (Octavia)  →  로드밸런서에 유동 IP 연동
        ↓
공유 볼륨 생성 · 마운트 (Manila)</code></pre>
    <div class="gm-feature-shot">
      <img src="/assets/img/posts/contrabass-network-diagram.png" alt="콘트라베이스 네트워크 구성도">
      <div class="gm-shot-caption">구성한 전체 네트워크 토폴로지 — Floating IP · Router · Load Balancer · VM</div>
    </div>
  </div>

</div>
