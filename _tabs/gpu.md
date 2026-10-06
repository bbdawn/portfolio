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
    margin-top: 0;
    margin-bottom: 0.8rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  #gpu-server .gm-card h3 i { color: var(--link-color); opacity: 0.85; }
  #gpu-server .gm-card p { font-size: 0.92rem; line-height: 1.75; opacity: 0.85; }
  #gpu-server .gm-card ul { font-size: 0.92rem; line-height: 1.8; opacity: 0.85; padding-left: 1.2rem; margin-bottom: 0; }
  #gpu-server .gm-card h4 { font-size: 0.95rem; font-weight: 700; margin: 1rem 0 0.4rem; }
  #gpu-server .gm-card h4:first-of-type { margin-top: 0.25rem; }

  #gpu-server .gm-note {
    font-size: 0.85rem;
    line-height: 1.8;
    padding: 0.7rem 1rem;
    border-left: 3px solid var(--link-color);
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.06);
    border-radius: 4px;
    margin: 0.75rem 0 0;
  }

  /* ── Hero ── */
  #gpu-server .gs-hero {
    border: 1px solid var(--border-color, #dee2e6);
    border-top: 4px solid var(--link-color);
    border-radius: 12px;
    padding: 1.5rem 1.5rem 1.25rem;
    margin-bottom: 1.5rem;
    background: var(--card-bg, rgba(0,0,0,0.015));
  }
  #gpu-server .gs-eyebrow {
    font-size: 0.72rem; font-weight: 700; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--link-color); margin-bottom: 0.35rem;
  }
  #gpu-server .gs-title { font-size: 1.45rem; font-weight: 800; letter-spacing: -0.02em; margin: 0 0 0.4rem !important; line-height: 1.35; }
  #gpu-server .gs-sub { font-size: 0.95rem; line-height: 1.7; opacity: 0.75; margin: 0 0 1.1rem; }
  #gpu-server .gs-meta {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.75rem;
    padding: 0.9rem 0; border-top: 1px solid var(--border-color, #dee2e6);
    border-bottom: 1px solid var(--border-color, #dee2e6); margin-bottom: 0.9rem;
  }
  #gpu-server .gs-meta-label { font-size: 0.7rem; font-weight: 700; opacity: 0.45; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 0.15rem; }
  #gpu-server .gs-meta-value { font-size: 0.88rem; font-weight: 600; line-height: 1.5; }
  #gpu-server .gm-chips { display: flex; flex-wrap: wrap; gap: 0.35rem; }
  #gpu-server .gm-chip {
    font-size: 0.76rem; padding: 0.15rem 0.6rem; border-radius: 999px;
    border: 1px solid var(--border-color, #dee2e6); white-space: nowrap;
  }

  /* ── Flow ── */
  #gpu-server .gs-flow {
    display: grid; grid-template-columns: 1fr auto 1fr auto 1fr; align-items: stretch; gap: 0.5rem;
    margin-bottom: 1.5rem;
  }
  #gpu-server .gs-step {
    border: 1px solid var(--border-color, #dee2e6); border-radius: 10px;
    padding: 0.85rem 1rem; text-align: center; background: var(--main-bg, #fff);
  }
  #gpu-server .gs-step-num { font-size: 0.7rem; font-weight: 700; color: var(--link-color); letter-spacing: 0.08em; }
  #gpu-server .gs-step-title { font-size: 0.95rem; font-weight: 700; margin: 0.15rem 0 0.2rem; }
  #gpu-server .gs-step-desc { font-size: 0.8rem; line-height: 1.55; opacity: 0.7; }
  #gpu-server .gs-arrow { display: flex; align-items: center; opacity: 0.35; }

  /* ── Contributions ── */
  #gpu-server .gs-contrib { display: flex; flex-direction: column; gap: 0.75rem; }
  #gpu-server .gs-item {
    display: grid; grid-template-columns: 2.2rem 1fr; gap: 0.75rem;
    border: 1px solid var(--border-color, #dee2e6); border-radius: 10px;
    padding: 0.9rem 1rem; background: var(--main-bg, #fff);
  }
  #gpu-server .gs-num {
    width: 2.2rem; height: 2.2rem; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.1); color: var(--link-color);
    font-weight: 800; font-size: 0.9rem;
  }
  #gpu-server .gs-item-title { font-size: 0.97rem; font-weight: 700; margin-bottom: 0.2rem; }
  #gpu-server .gs-item-desc { font-size: 0.88rem; line-height: 1.7; opacity: 0.8; }
  #gpu-server .gs-map { margin-top: 0.4rem; font-size: 0.8rem; display: flex; flex-wrap: wrap; align-items: center; gap: 0.35rem; }
  #gpu-server .gs-map-label { font-weight: 700; opacity: 0.5; }
  #gpu-server .gs-map .gm-chip { border-color: var(--link-color); color: var(--link-color); }
  #gpu-server .gs-item a.gs-link { font-size: 0.82rem; font-weight: 600; }

  /* ── Service intro ── */
  #gpu-server .gm-lead { font-size: 1rem !important; font-weight: 600; line-height: 1.7 !important; opacity: 1 !important; margin-bottom: 0.6rem; }
  #gpu-server .gm-points { list-style: none; padding-left: 0 !important; margin: 0 0 0.25rem; }
  #gpu-server .gm-points li { position: relative; padding-left: 1.4rem; }
  #gpu-server .gm-points li i { position: absolute; left: 0; top: 0.42rem; font-size: 0.8rem; color: var(--link-color); }
  #gpu-server .gm-value-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.9rem; margin-top: 0.9rem; }
  #gpu-server .gm-value {
    border: 1px solid var(--border-color, #dee2e6); border-radius: 8px;
    padding: 0.9rem 1rem; background: var(--main-bg, #fff);
  }
  #gpu-server .gm-value-title { font-size: 0.92rem; font-weight: 700; margin-bottom: 0.35rem; display: flex; align-items: center; gap: 0.45rem; }
  #gpu-server .gm-value-title i { color: var(--link-color); opacity: 0.85; }
  #gpu-server .gm-value-desc { font-size: 0.85rem; line-height: 1.65; opacity: 0.75; }
  #gpu-server .gm-value-desc ul { padding-left: 1rem; margin: 0; }
  #gpu-server .gm-value-desc .gm-chips { margin-top: 0.3rem; }

  #gpu-server .gs-section-title {
    font-size: 0.75rem; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase;
    opacity: 0.45; margin: 2rem 0 0.75rem;
  }

  @media (max-width: 768px) {
    #gpu-server .gm-value-grid, #gpu-server .gs-meta { grid-template-columns: 1fr; }
    #gpu-server .gs-flow { grid-template-columns: 1fr; }
    #gpu-server .gs-arrow { justify-content: center; transform: rotate(90deg); }
  }
</style>

<div id="gpu-server">

  <!-- ══════════ Hero ══════════ -->
  <div class="gs-hero">
    <div class="gs-eyebrow">Project · GPU Cloud Service</div>
    <h2 class="gs-title">KT Cloud PPP 「GPU Server」</h2>
    <p class="gs-sub">공공기관 전용 GPU 클라우드 서비스의 핵심 기능인 GPU Instance와 GPU 모니터링을 개발하고,<br>KT Cloud PPP 「GPU Server」 상품화 및 서비스 제공에 참여했습니다.</p>

    <div class="gs-meta">
      <div>
        <div class="gs-meta-label">소속</div>
        <div class="gs-meta-value">오케스트로<br>콘트라베이스 최적화팀</div>
      </div>
      <div>
        <div class="gs-meta-label">역할</div>
        <div class="gs-meta-value">GPU Instance · 모니터링<br>기능 개발</div>
      </div>
      <div>
        <div class="gs-meta-label">결과</div>
        <div class="gs-meta-value">KT Cloud PPP<br>「GPU Server」 상품화</div>
      </div>
    </div>

    <div class="gm-chips">
      <span class="gm-chip">OpenStack</span>
      <span class="gm-chip">GPU Passthrough</span>
      <span class="gm-chip">NVIDIA MIG</span>
      <span class="gm-chip">GPU Monitoring</span>
      <span class="gm-chip">공공 클라우드 (PPP)</span>
    </div>
  </div>

  <!-- ══════════ Flow ══════════ -->
  <div class="gs-flow">
    <div class="gs-step">
      <div class="gs-step-num">STEP 1</div>
      <div class="gs-step-title">기능 개발</div>
      <div class="gs-step-desc">GPU Passthrough·MIG 기반<br>GPU Instance · 모니터링</div>
    </div>
    <div class="gs-arrow"><i class="fas fa-chevron-right"></i></div>
    <div class="gs-step">
      <div class="gs-step-num">STEP 2</div>
      <div class="gs-step-title">서비스 적용</div>
      <div class="gs-step-desc">PPP 클라우드 환경에<br>GPU 기능 적용</div>
    </div>
    <div class="gs-arrow"><i class="fas fa-chevron-right"></i></div>
    <div class="gs-step">
      <div class="gs-step-num">STEP 3</div>
      <div class="gs-step-title">상품화</div>
      <div class="gs-step-desc">KT Cloud PPP<br>「GPU Server」 서비스 제공</div>
    </div>
  </div>

  <!-- ══════════ Contributions ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-user-cog"></i> 나의 기여</h3>
    <div class="gs-contrib">
      <div class="gs-item">
        <div class="gs-num">1</div>
        <div>
          <div class="gs-item-title">GPU Instance 기능 개발</div>
          <div class="gs-item-desc">GPU Passthrough와 MIG 방식으로 GPU를 인스턴스에 할당하는 GPU Instance 생성 및 관리 기능을 개발했습니다.</div>
          <div class="gs-map"><span class="gs-map-label">상품 기능 →</span><span class="gm-chip">GPU 서버 스펙(Flavor) 기반 서버 생성</span><span class="gm-chip">GPU 서버 상태 관리</span></div>
        </div>
      </div>
      <div class="gs-item">
        <div class="gs-num">2</div>
        <div>
          <div class="gs-item-title">GPU 모니터링 기능 개발</div>
          <div class="gs-item-desc">GPU Host와 GPU Instance 단위로 GPU 사용률, 메모리 사용률, 온도, 전력 사용량을 확인할 수 있는 모니터링 기능을 개발했습니다.</div>
          <div class="gs-map"><span class="gs-map-label">상품 기능 →</span><span class="gm-chip">자원 모니터링</span></div>
        </div>
      </div>
      <div class="gs-item">
        <div class="gs-num">3</div>
        <div>
          <div class="gs-item-title">상품화 및 서비스 제공</div>
          <div class="gs-item-desc">개발한 GPU 기능을 기반으로 KT Cloud PPP 「GPU Server」 상품화 및 서비스 제공에 참여했습니다.</div>
        </div>
      </div>
      <div class="gs-item">
        <div class="gs-num">4</div>
        <div>
          <div class="gs-item-title">GPU 운영 자동화</div>
          <div class="gs-item-desc">GPU Instance 운영 중 발생하는 mdev orphan 탐지와 MIG 프로파일 관리를 자동화하는 운영 도구를 만들었습니다.
            <a class="gs-link" href="{{ '/gpu-manager/' | relative_url }}">GPU Manager 보기 →</a></div>
        </div>
      </div>
    </div>
  </div>

  <div class="gs-section-title">About the Service</div>

  <div class="gm-card">
    <h3><i class="fas fa-cloud"></i> 서비스 소개</h3>
    <p class="gm-lead">KT Cloud PPP 「GPU Server」는 일반 Public Cloud 서비스 대비 강화된 보안성을 제공하는 공공기관 전용 Cloud 컴퓨팅 인프라 서비스입니다.</p>
    <ul class="gm-points">
      <li><i class="fas fa-check"></i>크기 조정이 가능한 컴퓨팅 인프라를 가상화하여 제공</li>
      <li><i class="fas fa-check"></i>서버들의 리소스는 PPP에서 안전하게 관리</li>
      <li><i class="fas fa-check"></i>고객 단독 사용 보장</li>
    </ul>

    <div class="gm-note">
      <strong>PPP 클라우드란?</strong><br>
      PPP(Public Private Partnership, 민관협력형) 클라우드는 공공과 민간이 협력하여 클라우드 환경을 함께 설계하고 운영하는 클라우드입니다.
      민간의 경험과 기술력, 자본을 활용해 공공 서비스를 효율적으로 제공하기 위해 만들어진 모델입니다.
    </div>

    <div class="gm-value-grid">
      <div class="gm-value">
        <div class="gm-value-title"><i class="fas fa-shield-alt"></i> 안전한 데이터 처리</div>
        <div class="gm-value-desc">
          <ul>
            <li>보안 인증 획득</li>
            <li>물리적 FW/IPS로 대규모 공격에서 안전</li>
            <li>보유 민감정보는 별도 Zone에서 보호</li>
          </ul>
        </div>
      </div>
      <div class="gm-value">
        <div class="gm-value-title"><i class="fas fa-mouse-pointer"></i> 간편한 Server 생성</div>
        <div class="gm-value-desc">GUI 기반의 간편한 클라우드 GPU Server 생성</div>
      </div>
      <div class="gm-value">
        <div class="gm-value-title"><i class="fas fa-chart-line"></i> 자원 모니터링</div>
        <div class="gm-value-desc">
          GPU Server 자원에 대한 가시성 제공
          <div class="gm-chips">
            <span class="gm-chip">GPU 사용률</span>
            <span class="gm-chip">GPU 메모리 사용률</span>
            <span class="gm-chip">GPU 온도</span>
            <span class="gm-chip">GPU 전력 사용량</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-th-list"></i> 주요 기능</h3>

    <h4>GPU 서버 스펙(Flavor) 기반 서버 생성</h4>
    <p>GPU 모델과 GPU 개수에 따라 구성된 GPU 서버 스펙(Flavor)을 선택하여 손쉽게 서버를 생성할 수 있습니다. GPU 서버 전용 이미지와 함께 원하는 서버 스펙을 선택하여 GPU 환경을 간편하게 구성할 수 있습니다.</p>

    <h4>GPU 서버 상태 관리</h4>
    <p>서비스 운영 상황에 따라 GPU 서버를 시작, 정지, 재시작, 변경하거나 삭제할 수 있습니다.</p>
    <div class="gm-note">서버 상태에 따라 과금 여부가 달라질 수 있습니다.</div>

    <h4>GPU Host, GPU Instance 모니터링</h4>
    <p>GPU Host와 GPU Instance 단위로 GPU 사용률, GPU 메모리 사용률, GPU 온도, GPU 전력 사용량 등 GPU 자원 상태를 모니터링할 수 있습니다.</p>
  </div>

</div>
