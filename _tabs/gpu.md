---
layout: page
title: GPU
icon: fas fa-microchip
order: 2
permalink: /gpu/
---

<style>
  #gpu-server * { box-sizing: border-box; }
  #gpu-server { margin: -0.5rem 0 0; }

  #gpu-server .gm-card {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 10px;
    padding: 1.25rem 1.4rem;
    margin-bottom: 1.25rem;
    background: var(--card-bg, rgba(0,0,0,0.015));
  }
  #gpu-server .gm-card h3 {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 0.6rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  #gpu-server .gm-card h3 i { color: var(--link-color); opacity: 0.85; }
  #gpu-server .gm-card p { font-size: 0.92rem; line-height: 1.75; opacity: 0.85; }

  #gpu-server .gm-note {
    font-size: 0.85rem;
    line-height: 1.8;
    padding: 0.7rem 1rem;
    border-left: 3px solid var(--link-color);
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.06);
    border-radius: 4px;
    margin: 0.75rem 0;
  }

  #gpu-server .gm-compare-badge {
    display: inline-block; font-size: 0.72rem; font-weight: 700;
    border-radius: 4px; padding: 0.1rem 0.5rem; margin-right: 0.4rem;
  }
  #gpu-server .gm-compare-badge.dev { background: rgba(var(--bs-primary-rgb, 13,110,253), 0.12); color: var(--link-color); }
  #gpu-server .gm-compare-badge.after { background: rgba(40,167,69,0.12); color: #28a745; }

  /* 3칸 박스 (특징 / 흐름) */
  #gpu-server .gs-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.75rem; margin: 0.9rem 0 0.25rem; }
  #gpu-server .gs-box {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px;
    padding: 0.9rem 1rem;
    background: var(--main-bg, #fff);
  }
  #gpu-server .gs-box-icon {
    width: 2rem; height: 2rem; border-radius: 8px;
    display: flex; align-items: center; justify-content: center;
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.1); color: var(--link-color);
    margin-bottom: 0.55rem;
  }
  #gpu-server .gs-box-title { font-size: 0.92rem; font-weight: 700; margin-bottom: 0.25rem; }
  #gpu-server .gs-box-desc { font-size: 0.83rem; line-height: 1.65; opacity: 0.75; }

  /* 흐름 */
  #gpu-server .gs-flow { display: grid; grid-template-columns: 1fr auto 1fr auto 1fr; gap: 0.5rem; align-items: stretch; margin-top: 0.9rem; }
  #gpu-server .gs-flow .gs-box { text-align: center; }
  #gpu-server .gs-flow .gs-box-icon { margin: 0 auto 0.55rem; }
  #gpu-server .gs-step { font-size: 0.7rem; font-weight: 700; letter-spacing: 0.08em; color: var(--link-color); }
  #gpu-server .gs-arrow { display: flex; align-items: center; opacity: 0.35; }

  /* 담당 업무 */
  #gpu-server .gs-task { padding: 0.9rem 0; border-top: 1px dashed var(--border-color, #dee2e6); }
  #gpu-server .gs-task:first-of-type { border-top: none; padding-top: 0.25rem; }
  #gpu-server .gs-task-title { font-size: 0.97rem; font-weight: 700; margin-bottom: 0.3rem; display: flex; align-items: center; gap: 0.5rem; }
  #gpu-server .gs-task-title i { color: var(--link-color); opacity: 0.85; width: 1.1rem; text-align: center; }
  #gpu-server .gs-task p { margin-bottom: 0.35rem; }
  #gpu-server .gs-map { font-size: 0.82rem; opacity: 0.85; }

  /* GPU 할당 방식 다이어그램 */
  #gpu-server .gs-diagram {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px;
    padding: 0.75rem;
    margin: 0.75rem 0 0.5rem;
    background: var(--code-bg, #f6f6f6);
    overflow-x: auto;
  }
  #gpu-server .gs-diagram svg { display: block; width: 100%; min-width: 520px; height: auto; color: var(--text-color, #333); }
  #gpu-server .gs-diagram .acc { fill: var(--link-color); }
  #gpu-server .gs-diagram .acc-s { stroke: var(--link-color); }

  /* 주요 기능 */
  #gpu-server .gs-feat-title { font-size: 0.95rem; font-weight: 700; margin: 1rem 0 0.35rem; display: flex; align-items: center; gap: 0.5rem; }
  #gpu-server .gs-feat-title:first-of-type { margin-top: 0.25rem; }
  #gpu-server .gs-feat-title i { color: var(--link-color); opacity: 0.85; width: 1.1rem; text-align: center; }

  @media (max-width: 768px) {
    #gpu-server .gs-grid, #gpu-server .gs-flow { grid-template-columns: 1fr; }
    #gpu-server .gs-arrow { justify-content: center; transform: rotate(90deg); }
  }
</style>

<div id="gpu-server">

  <!-- ══════════ 개요 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-lightbulb"></i> 개요</h3>
    <p>KT Cloud PPP 「GPU Server」는 일반 Public Cloud 서비스 대비 강화된 보안성을 제공하는 공공기관 전용 Cloud 컴퓨팅 인프라 서비스입니다.<br>
    크기 조정이 가능한 컴퓨팅 인프라를 가상화하여 제공하되, 서버들의 리소스는 PPP에서 안전하게 관리하고 고객 단독 사용이 보장됩니다.</p>
    <div class="gs-grid">
      <div class="gs-box">
        <div class="gs-box-icon"><i class="fas fa-shield-alt"></i></div>
        <div class="gs-box-title">안전한 데이터 처리</div>
        <div class="gs-box-desc">보안 인증 획득, 물리적 FW/IPS로 대규모 공격에서 안전, 보유 민감정보는 별도 Zone에서 보호</div>
      </div>
      <div class="gs-box">
        <div class="gs-box-icon"><i class="fas fa-mouse-pointer"></i></div>
        <div class="gs-box-title">간편한 Server 생성</div>
        <div class="gs-box-desc">GUI 기반의 간편한 클라우드 GPU Server 생성</div>
      </div>
      <div class="gs-box">
        <div class="gs-box-icon"><i class="fas fa-chart-line"></i></div>
        <div class="gs-box-title">자원 모니터링</div>
        <div class="gs-box-desc">GPU 사용률, GPU 메모리 사용률, GPU 온도, GPU 전력 사용량 등 GPU Server 자원에 대한 가시성 제공</div>
      </div>
    </div>
    <div class="gm-note">
      <strong>PPP 클라우드란?</strong><br>
      PPP(Public Private Partnership, 민관협력형) 클라우드는 공공과 민간이 협력하여 클라우드 환경을 함께 설계하고 운영하는 클라우드입니다.
      민간의 경험과 기술력, 자본을 활용해 공공 서비스를 효율적으로 제공하기 위해 만들어진 모델입니다.
    </div>
  </div>

  <!-- ══════════ 기술에서 상품까지 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-route"></i> 기술에서 상품까지</h3>
    <p>GPU Instance와 모니터링 기능 개발부터 실제 서비스 적용, 「GPU Server」 상품화까지 전 과정에 참여했습니다.</p>
    <div class="gs-flow">
      <div class="gs-box">
        <div class="gs-box-icon"><i class="fas fa-code"></i></div>
        <div class="gs-step">STEP 1</div>
        <div class="gs-box-title">기능 개발</div>
        <div class="gs-box-desc">GPU Passthrough·MIG 기반<br>GPU Instance · 모니터링</div>
      </div>
      <div class="gs-arrow"><i class="fas fa-chevron-right"></i></div>
      <div class="gs-box">
        <div class="gs-box-icon"><i class="fas fa-cloud-upload-alt"></i></div>
        <div class="gs-step">STEP 2</div>
        <div class="gs-box-title">서비스 적용</div>
        <div class="gs-box-desc">PPP 클라우드 환경에<br>GPU 기능 적용</div>
      </div>
      <div class="gs-arrow"><i class="fas fa-chevron-right"></i></div>
      <div class="gs-box">
        <div class="gs-box-icon"><i class="fas fa-box-open"></i></div>
        <div class="gs-step">STEP 3</div>
        <div class="gs-box-title">상품화</div>
        <div class="gs-box-desc">KT Cloud PPP<br>「GPU Server」 서비스 제공</div>
      </div>
    </div>
  </div>

  <!-- ══════════ 담당 업무 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-user-cog"></i> 담당 업무</h3>

    <div class="gs-task">
      <div class="gs-task-title"><i class="fas fa-microchip"></i> GPU Instance 기능 개발</div>
      <p>GPU Passthrough와 MIG 방식으로 GPU를 인스턴스에 할당하는 GPU Instance 생성 및 관리 기능을 개발했습니다.</p>
      <div class="gs-map"><span class="gm-compare-badge after">상품 기능</span>GPU 서버 스펙(Flavor) 기반 서버 생성 · GPU 서버 상태 관리</div>
    </div>

    <div class="gs-task">
      <div class="gs-task-title"><i class="fas fa-chart-area"></i> GPU 모니터링 기능 개발</div>
      <p>GPU Host와 GPU Instance 단위로 GPU 자원 상태를 확인할 수 있는 모니터링 기능을 개발했습니다.</p>
      <div class="gs-map"><span class="gm-compare-badge after">상품 기능</span>GPU Host, GPU Instance 모니터링</div>
    </div>

    <div class="gs-task">
      <div class="gs-task-title"><i class="fas fa-box-open"></i> 상품화 및 서비스 제공</div>
      <p>개발한 GPU 기능을 기반으로 KT Cloud PPP 「GPU Server」 상품화 및 서비스 제공에 참여했습니다.</p>
    </div>

    <div class="gs-task">
      <div class="gs-task-title"><i class="fas fa-toolbox"></i> GPU 운영 자동화</div>
      <p>GPU Instance 운영을 위한 mdev orphan 탐지 및 MIG 프로파일 관리 자동화 도구를 개발했습니다.</p>
      <div class="gs-map"><span class="gm-compare-badge dev">운영 도구</span><a href="{{ '/gpu-manager/' | relative_url }}">GPU Manager 보기 →</a></div>
    </div>
  </div>

  <!-- ══════════ GPU 할당 방식 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-layer-group"></i> GPU 할당 방식</h3>
    <p>GPU Instance 기능은 워크로드 성격에 따라 두 가지 방식으로 물리 GPU를 인스턴스에 할당합니다.</p>
    <div class="gs-diagram">
      <svg viewBox="0 0 640 230" xmlns="http://www.w3.org/2000/svg" font-family="inherit" role="img" aria-label="GPU Passthrough와 MIG 할당 방식 비교">
        <g fill="none" stroke="currentColor" stroke-opacity="0.35" stroke-width="1.5">
          <rect x="10" y="10" width="300" height="210" rx="10"/>
          <rect x="330" y="10" width="300" height="210" rx="10"/>
        </g>
        <text x="160" y="38" text-anchor="middle" font-size="14" font-weight="700" fill="currentColor">GPU Passthrough</text>
        <text x="480" y="38" text-anchor="middle" font-size="14" font-weight="700" fill="currentColor">MIG (Multi-Instance GPU)</text>
        <!-- Passthrough -->
        <rect x="60" y="60" width="200" height="50" rx="6" class="acc" fill-opacity="0.85"/>
        <text x="160" y="90" text-anchor="middle" font-size="12" font-weight="700" fill="#fff">물리 GPU (전체)</text>
        <line x1="160" y1="110" x2="160" y2="145" class="acc-s" stroke-width="2"/>
        <polygon points="154,140 166,140 160,150" class="acc"/>
        <rect x="90" y="152" width="140" height="40" rx="6" fill="none" stroke="currentColor" stroke-opacity="0.6" stroke-width="1.5"/>
        <text x="160" y="177" text-anchor="middle" font-size="12" fill="currentColor">VM 1개</text>
        <text x="160" y="210" text-anchor="middle" font-size="11" fill="currentColor" fill-opacity="0.6">GPU 1개를 VM 1개가 독점</text>
        <!-- MIG -->
        <rect x="380" y="60" width="200" height="50" rx="6" fill="none" class="acc-s" stroke-width="1.5"/>
        <rect x="384" y="64" width="62" height="42" rx="4" class="acc" fill-opacity="0.85"/>
        <rect x="449" y="64" width="62" height="42" rx="4" class="acc" fill-opacity="0.6"/>
        <rect x="514" y="64" width="62" height="42" rx="4" class="acc" fill-opacity="0.4"/>
        <text x="415" y="89" text-anchor="middle" font-size="10" font-weight="700" fill="#fff">slice</text>
        <text x="480" y="89" text-anchor="middle" font-size="10" font-weight="700" fill="#fff">slice</text>
        <text x="545" y="89" text-anchor="middle" font-size="10" font-weight="700" fill="#fff">slice</text>
        <g class="acc-s" stroke-width="2">
          <line x1="415" y1="110" x2="415" y2="145"/>
          <line x1="480" y1="110" x2="480" y2="145"/>
          <line x1="545" y1="110" x2="545" y2="145"/>
        </g>
        <polygon points="409,140 421,140 415,150" class="acc"/>
        <polygon points="474,140 486,140 480,150" class="acc"/>
        <polygon points="539,140 551,140 545,150" class="acc"/>
        <g fill="none" stroke="currentColor" stroke-opacity="0.6" stroke-width="1.5">
          <rect x="387" y="152" width="56" height="40" rx="6"/>
          <rect x="452" y="152" width="56" height="40" rx="6"/>
          <rect x="517" y="152" width="56" height="40" rx="6"/>
        </g>
        <text x="415" y="177" text-anchor="middle" font-size="12" fill="currentColor">VM</text>
        <text x="480" y="177" text-anchor="middle" font-size="12" fill="currentColor">VM</text>
        <text x="545" y="177" text-anchor="middle" font-size="12" fill="currentColor">VM</text>
        <text x="480" y="210" text-anchor="middle" font-size="11" fill="currentColor" fill-opacity="0.6">하드웨어 파티션(mdev)을 여러 VM이 공유</text>
      </svg>
    </div>
    <p style="font-size:0.85rem; opacity:0.7;">대규모 학습처럼 GPU 성능을 온전히 써야 하는 워크로드는 Passthrough, 다수의 경량 추론·개발 워크로드는 MIG가 유리합니다. 자세한 비교는 <a href="{{ '/gpu-manager/' | relative_url }}">GPU Manager</a>의 "GPU 가상화 개념" 탭에 정리했습니다.</p>
  </div>

  <!-- ══════════ 주요 기능 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-th-list"></i> 주요 기능</h3>

    <div class="gs-feat-title"><i class="fas fa-server"></i> GPU 서버 스펙(Flavor) 기반 서버 생성</div>
    <p>GPU 모델과 GPU 개수에 따라 구성된 GPU 서버 스펙(Flavor)을 선택하여 손쉽게 서버를 생성할 수 있습니다. GPU 서버 전용 이미지와 함께 원하는 서버 스펙을 선택하여 GPU 환경을 간편하게 구성할 수 있습니다.</p>

    <div class="gs-feat-title"><i class="fas fa-power-off"></i> GPU 서버 상태 관리</div>
    <p>서비스 운영 상황에 따라 GPU 서버를 시작, 정지, 재시작, 변경하거나 삭제할 수 있습니다.</p>
    <div class="gm-note">서버 상태에 따라 과금 여부가 달라질 수 있습니다.</div>

    <div class="gs-feat-title"><i class="fas fa-chart-area"></i> GPU Host, GPU Instance 모니터링</div>
    <p>GPU Host와 GPU Instance 단위로 GPU 사용률, GPU 메모리 사용률, GPU 온도, GPU 전력 사용량 등 GPU 자원 상태를 모니터링할 수 있습니다.</p>
  </div>

</div>
