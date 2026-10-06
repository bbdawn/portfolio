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

  #gpu-server .gm-value-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0.9rem;
    margin-top: 0.75rem;
  }
  #gpu-server .gm-value {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px;
    padding: 0.9rem 1rem;
    background: var(--main-bg, #fff);
  }
  #gpu-server .gm-value-title {
    font-size: 0.92rem;
    font-weight: 700;
    margin-bottom: 0.35rem;
    display: flex;
    align-items: center;
    gap: 0.45rem;
  }
  #gpu-server .gm-value-title i { color: var(--link-color); opacity: 0.85; }
  #gpu-server .gm-value-desc { font-size: 0.85rem; line-height: 1.65; opacity: 0.75; }

  @media (max-width: 768px) {
    #gpu-server .gm-value-grid { grid-template-columns: 1fr; }
  }
</style>

<div id="gpu-server">

  <div class="gm-card">
    <h3><i class="fas fa-lightbulb"></i> 개요</h3>
    <p>KT Cloud PPP 「GPU Server」는 일반 Public Cloud 서비스 대비 강화된 보안성을 제공하는 공공기관 전용 Cloud 컴퓨팅 인프라 서비스입니다.<br>
    크기 조정이 가능한 컴퓨팅 인프라를 가상화하여 제공하되, 서버들의 리소스는 PPP에서 안전하게 관리하고 고객 단독 사용이 보장됩니다.</p>

    <div class="gm-value-grid">
      <div class="gm-value">
        <div class="gm-value-title"><i class="fas fa-shield-alt"></i> 안전한 데이터 처리</div>
        <div class="gm-value-desc">보안 인증 획득, 물리적 FW/IPS로 대규모 공격에서 안전, 보유 민감정보는 별도 Zone에서 보호</div>
      </div>
      <div class="gm-value">
        <div class="gm-value-title"><i class="fas fa-mouse-pointer"></i> 간편한 Server 생성</div>
        <div class="gm-value-desc">GUI 기반의 간편한 클라우드 GPU Server 생성</div>
      </div>
      <div class="gm-value">
        <div class="gm-value-title"><i class="fas fa-chart-line"></i> 자원 모니터링</div>
        <div class="gm-value-desc">GPU Server 자원에 대한 가시성(GPU 사용률, GPU 메모리 사용률, GPU 온도, GPU 전력 사용량 등) 제공</div>
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
  </div>

  <div class="gm-card">
    <h3><i class="fas fa-user-cog"></i> 담당 역할</h3>
    <ul>
      <li>GPU Passthrough·MIG 기반 GPU Instance 및 모니터링 기능 개발</li>
      <li>KT Cloud PPP 「GPU Server」 상품화 및 서비스 제공</li>
    </ul>
  </div>

</div>
