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
  #gpu-server .gm-card ul { font-size: 0.92rem; line-height: 1.8; opacity: 0.85; padding-left: 1.2rem; }

  #gpu-server .gm-note {
    font-size: 0.85rem;
    line-height: 1.8;
    padding: 0.7rem 1rem;
    border-left: 3px solid var(--link-color);
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.06);
    border-radius: 4px;
    margin: 0.75rem 0;
  }

  #gpu-server table.gm-table {
    width: 100%;
    font-size: 0.88rem;
    border-collapse: collapse;
    margin: 0.75rem 0 0.25rem;
  }
  #gpu-server table.gm-table th,
  #gpu-server table.gm-table td {
    border: 1px solid var(--border-color, #dee2e6);
    padding: 0.5rem 0.7rem;
    text-align: left;
    vertical-align: top;
    white-space: normal;
    word-break: keep-all;
  }
  #gpu-server table.gm-table td:first-child { min-width: 8.5rem; }
  #gpu-server table.gm-table th { background: rgba(0,0,0,0.03); }
</style>

<div id="gpu-server">

  <!-- ══════════ 개요 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-lightbulb"></i> 개요</h3>
    <p>KT Cloud PPP 「GPU Server」는 일반 Public Cloud 서비스 대비 강화된 보안성을 제공하는 공공기관 전용 Cloud 컴퓨팅 인프라 서비스입니다.<br>
    크기 조정이 가능한 컴퓨팅 인프라를 가상화하여 제공하되, 서버들의 리소스는 PPP에서 안전하게 관리하고 고객 단독 사용이 보장됩니다.</p>
    <p>GPU Passthrough·MIG 기반 GPU Instance와 GPU 모니터링 기능을 개발하고, 이 기능을 바탕으로 「GPU Server」 상품화 및 서비스 제공에 참여했습니다.</p>
    <div class="gm-note">
      <strong>PPP 클라우드란?</strong><br>
      PPP(Public Private Partnership, 민관협력형) 클라우드는 공공과 민간이 협력하여 클라우드 환경을 함께 설계하고 운영하는 클라우드입니다.
      민간의 경험과 기술력, 자본을 활용해 공공 서비스를 효율적으로 제공하기 위해 만들어진 모델입니다.
    </div>
  </div>

  <!-- ══════════ 담당 업무 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-user-cog"></i> 담당 업무</h3>
    <table class="gm-table">
      <tr><th>업무</th><th>내용</th><th>상품 기능</th></tr>
      <tr>
        <td>GPU Instance 기능 개발</td>
        <td>GPU Passthrough와 MIG 방식으로 GPU를 인스턴스에 할당하는 GPU Instance 생성 및 관리 기능 개발</td>
        <td>GPU 서버 스펙(Flavor) 기반 서버 생성, GPU 서버 상태 관리</td>
      </tr>
      <tr>
        <td>GPU 모니터링 기능 개발</td>
        <td>GPU Host와 GPU Instance 단위 GPU 자원 모니터링 기능 개발</td>
        <td>GPU Host, GPU Instance 모니터링</td>
      </tr>
      <tr>
        <td>상품화 및 서비스 제공</td>
        <td>개발한 GPU 기능을 기반으로 KT Cloud PPP 「GPU Server」 상품화 및 서비스 제공 참여</td>
        <td>-</td>
      </tr>
      <tr>
        <td>GPU 운영 자동화</td>
        <td>GPU Instance 운영을 위한 mdev orphan 탐지 및 MIG 프로파일 관리 자동화 도구 개발 (<a href="{{ '/gpu-manager/' | relative_url }}">GPU Manager</a>)</td>
        <td>-</td>
      </tr>
    </table>
  </div>

  <!-- ══════════ 서비스 특징 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-star"></i> 서비스 특징</h3>
    <table class="gm-table">
      <tr><th>특징</th><th>내용</th></tr>
      <tr>
        <td>안전한 데이터 처리</td>
        <td>보안 인증 획득, 물리적 FW/IPS로 대규모 공격에서 안전, 보유 민감정보는 별도 Zone에서 보호</td>
      </tr>
      <tr>
        <td>간편한 Server 생성</td>
        <td>GUI 기반의 간편한 클라우드 GPU Server 생성</td>
      </tr>
      <tr>
        <td>자원 모니터링</td>
        <td>GPU Server 자원에 대한 가시성(GPU 사용률, GPU 메모리 사용률, GPU 온도, GPU 전력 사용량 등) 제공</td>
      </tr>
    </table>
  </div>

  <!-- ══════════ 주요 기능 ══════════ -->
  <div class="gm-card">
    <h3><i class="fas fa-th-list"></i> 주요 기능</h3>

    <p><strong>1. GPU 서버 스펙(Flavor) 기반 서버 생성</strong></p>
    <p>GPU 모델과 GPU 개수에 따라 구성된 GPU 서버 스펙(Flavor)을 선택하여 손쉽게 서버를 생성할 수 있습니다. GPU 서버 전용 이미지와 함께 원하는 서버 스펙을 선택하여 GPU 환경을 간편하게 구성할 수 있습니다.</p>

    <p><strong>2. GPU 서버 상태 관리</strong></p>
    <p>서비스 운영 상황에 따라 GPU 서버를 시작, 정지, 재시작, 변경하거나 삭제할 수 있습니다.</p>
    <div class="gm-note">서버 상태에 따라 과금 여부가 달라질 수 있습니다.</div>

    <p><strong>3. GPU Host, GPU Instance 모니터링</strong></p>
    <p>GPU Host와 GPU Instance 단위로 GPU 사용률, GPU 메모리 사용률, GPU 온도, GPU 전력 사용량 등 GPU 자원 상태를 모니터링할 수 있습니다.</p>
  </div>

</div>
