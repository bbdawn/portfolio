---
layout: page
title: Data Center
icon: fas fa-server
order: 4
permalink: /data-center/
---

<style>
  #data-center * { box-sizing: border-box; }
  #data-center { margin: -0.5rem 0 0; }
  #data-center .gm-tabs {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1.5rem;
  }
  #data-center .gm-tab-btn {
    border: 1.5px solid var(--border-color, #dee2e6);
    background: var(--main-bg, #fff);
    color: var(--text-color, #333);
    border-radius: 8px;
    padding: 0.5rem 1rem;
    font-size: 0.88rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.15s;
  }
  #data-center .gm-tab-btn:hover { border-color: var(--link-color); }
  #data-center .gm-tab-btn.active {
    background: var(--link-color);
    border-color: var(--link-color);
    color: #fff;
  }

  #data-center .gm-panel { display: none; }
  #data-center .gm-panel.active { display: block; }

  #data-center .gm-card {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 10px;
    padding: 1.25rem 1.4rem;
    margin-bottom: 1.25rem;
    background: var(--card-bg, rgba(0,0,0,0.015));
  }
  #data-center .gm-card h3 {
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 0.6rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }
  #data-center .gm-card h3 i { color: var(--link-color); opacity: 0.85; }
  #data-center .gm-card p { font-size: 0.92rem; line-height: 1.75; opacity: 0.85; }
  #data-center .gm-card ul { font-size: 0.92rem; line-height: 1.8; opacity: 0.85; padding-left: 1.2rem; }

  #data-center .gm-note {
    font-size: 0.85rem;
    line-height: 1.8;
    padding: 0.7rem 1rem;
    border-left: 3px solid var(--link-color);
    background: rgba(var(--bs-primary-rgb, 13,110,253), 0.06);
    border-radius: 4px;
    margin: 0.75rem 0;
  }

  #data-center table.gm-table {
    width: 100%;
    font-size: 0.88rem;
    border-collapse: collapse;
    margin: 0.75rem 0 0.25rem;
  }
  #data-center table.gm-table th,
  #data-center table.gm-table td {
    border: 1px solid var(--border-color, #dee2e6);
    padding: 0.5rem 0.7rem;
    text-align: left;
    vertical-align: top;
  }
  #data-center table.gm-table th { background: rgba(0,0,0,0.03); }

  #data-center .gm-feature-shot {
    border: 1px solid var(--border-color, #dee2e6);
    border-radius: 8px;
    padding: 0.75rem;
    margin: 0.75rem 0 1rem;
    background: var(--code-bg, #f6f6f6);
  }
  #data-center .gm-feature-shot img { max-width: 100%; height: auto; border-radius: 6px; display: block; margin: 0 auto; }
  #data-center .gm-shot-caption {
    font-size: 0.8rem;
    opacity: 0.65;
    margin-top: 0.35rem;
    text-align: center;
  }
  #data-center pre { overflow-x: auto; font-size: 0.82rem; line-height: 1.6; }
  #data-center .gm-compare-badge {
    display: inline-block; font-size: 0.72rem; font-weight: 700;
    border-radius: 4px; padding: 0.1rem 0.5rem; margin-right: 0.4rem;
  }
  #data-center .gm-compare-badge.before { background: rgba(220,53,69,0.12); color: #dc3545; }
  #data-center .gm-compare-badge.after { background: rgba(40,167,69,0.12); color: #28a745; }
</style>

<div id="data-center">

  <div class="gm-tabs">
    <button class="gm-tab-btn active" data-panel="overview">데이터센터 랙 구성도</button>
    <button class="gm-tab-btn" data-panel="provider">멀티 공급자 자원 공유</button>
  </div>

  <!-- ══════════ 데이터센터 랙 구성도 ══════════ -->
  <div class="gm-panel active" id="panel-overview">
    <div class="gm-card">
      <h3><i class="fas fa-lightbulb"></i> 개요</h3>
      <p>데이터센터의 물리/가상 인프라 구조를 시각화하는 프로젝트입니다. 랙에 배치된 서버·스위치·스토리지의 위치와 상태, 장비 간 물리 네트워크 연결, 그리고 그 위에서 동작하는 OpenStack 가상 네트워크와 인스턴스까지 하나의 흐름으로 보여줍니다.</p>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-th-list"></i> 주요 기능</h3>
      <table class="gm-table">
        <tr><th>기능</th><th>내용</th><th>데이터 소스</th></tr>
        <tr>
          <td><strong>랙 구성도</strong></td>
          <td>랙 단위 자원 배치와 서버 상태 시각화</td>
          <td>IPMI</td>
        </tr>
        <tr>
          <td><strong>물리 네트워크 토폴로지</strong></td>
          <td>서버 ↔ 스위치 포트 단위 연결 시각화</td>
          <td>SNMP</td>
        </tr>
        <tr>
          <td><strong>가상 네트워크 구성도</strong></td>
          <td>VLAN별 연결된 인스턴스 매핑·시각화</td>
          <td>OpenStack</td>
        </tr>
        <tr>
          <td><strong>멀티 공급자 자원 공유</strong></td>
          <td>공급자 간 Switch 중복 등록 제거, 1회 등록 후 참조</td>
          <td>SNMP</td>
        </tr>
      </table>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-server"></i> 랙 구성도</h3>
      <p>랙에서 호스트, 스위치, 스토리지의 위치 및 서버 상태 정보를 표시합니다.</p>
      <div class="gm-feature-shot">
        <img src="/assets/img/posts/rack-topology-rack-view.png" alt="랙 구성도 화면 - 랙별 장비 배치 및 서버 상세 정보">
        <div class="gm-shot-caption">랙 목록과 개별 장비의 상태·온도·팬 속도 등 상세 정보를 확인하는 랙 구성도 화면</div>
      </div>
      <ul>
        <li>Server, Storage, Switch 등 물리 자원 등록 및 관리</li>
        <li>랙 단위 자원 배치 시각화</li>
        <li>IPMI를 통해 각 서버의 실시간 자원 상태 정보(전원 상태, 센서 정보 등) 수집 및 표시</li>
        <li>실제 랙 이미지 위에 서버/스위치/스토리지 박스를 배치하고, 시스템 상태에 따라 색상 변화로 표시</li>
        <li>호스트 사양 및 관리 정보 제공</li>
      </ul>
      <div class="gm-note">
        <strong>활용</strong> — 물리적 장비 위치 파악 용이 · 원격에서 서버 상태 확인 및 이상 감지
      </div>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-network-wired"></i> 물리 네트워크 토폴로지</h3>
      <p>랙 구성도에 등록한 정보를 기반으로 호스트 및 스위치 연결정보를 표시합니다. 서버와 스위치 간 포트 단위 연결을 시각화하며, IPMI/SNMP 수집 데이터를 활용해 실제 연결 상태를 반영합니다.</p>
      <div class="gm-feature-shot">
        <img src="/assets/img/posts/rack-topology-physical-network-view.png" alt="물리 네트워크 구성도 화면 - 스위치/장비 포트 연결 및 스위치 상세 정보">
        <div class="gm-shot-caption">스위치와 서버 간 포트 연결을 시각화하고, 스위치 클릭 시 제조사·SNMP·APIC 등 상세 정보를 확인하는 화면</div>
      </div>
      <ul>
        <li>랙 구성도에 등록된 호스트와 스위치 정보를 기반으로 물리적 네트워크 연결 상태를 자동으로 시각화</li>
        <li>호스트의 특정 NIC 포트가 스위치의 어떤 포트에 연결되었는지 라인으로 표시</li>
        <li>SNMP 연동을 통해 각 스위치의 실시간 상태 정보를 표시</li>
        <li>호스트 및 스위치 아이콘 간 연결 라인, 포트 번호 표시</li>
      </ul>
      <div class="gm-note">
        <strong>활용</strong> — 네트워크 케이블링 오류 신속 파악 · 물리적 연결 문제 발생 시 빠른 원인 분석
      </div>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-project-diagram"></i> 가상 네트워크 구성도</h3>
      <p>물리 네트워크 호스트에 설치된 Contrabass Engine 내 가상 네트워크(VLAN 기반)에 연결된 가상 머신(VM) 정보를 시각적으로 표현합니다. OpenStack 기반으로 VLAN별 연결된 인스턴스를 매핑·시각화합니다.</p>
      <div class="gm-feature-shot">
        <img src="/assets/img/posts/rack-topology-virtual-network-view.png" alt="가상 네트워크 구성도 화면 - 네트워크/프로젝트별 인스턴스 매핑 및 상세 정보">
        <div class="gm-shot-caption">네트워크 디렉토리 트리와 프로젝트별 인스턴스 현황을 함께 보여주고, 인스턴스 클릭 시 상태·고정 IP 등 상세 정보를 확인하는 화면</div>
      </div>
    </div>
  </div>

  <!-- ══════════ 멀티 공급자 자원 공유 ══════════ -->
  <div class="gm-panel" id="panel-provider">
    <div class="gm-card">
      <h3><i class="fas fa-share-alt"></i> 개요</h3>
      <p>데이터센터 랙 토폴로지 시스템에서 공급자(Provider) 간 자원 중복 등록 문제를 해결하는 기능입니다.</p>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-sitemap"></i> 계층 구조</h3>
      <p>자원은 아래와 같은 4단계 계층으로 구성됩니다.</p>
<pre><code>Provider (공급자)
└── Datacenter (데이터센터)
    └── Rack (랙)
        └── Resource (서버 / 스위치 / 스토리지)</code></pre>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-exclamation-triangle"></i> 문제 상황</h3>
      <p><span class="gm-compare-badge before">BEFORE</span>기존에는 Switch가 여러 공급자에 중복 등록될 수 있었습니다. 동일한 물리 스위치가 여러 공급자에 각각 등록되면:</p>
      <ul>
        <li>같은 스위치에 SNMP 요청이 공급자 수만큼 반복 발생</li>
        <li>불필요한 네트워크 부하 및 스위치 응답 지연</li>
        <li>데이터 일관성 문제 (공급자마다 다른 수집 결과)</li>
      </ul>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-check-circle"></i> 해결 방법: 자원 공유 설계</h3>
      <p><span class="gm-compare-badge after">AFTER</span>Switch를 한 번만 등록하고, 다른 공급자에서는 불러오기(import) 방식으로 재사용합니다.</p>
<pre><code>[공급자 A]              [공급자 B]
  Rack A                 Rack B
  └── Switch X  ←─────── Switch X (불러오기)
       (원본)              (참조)</code></pre>
      <ul>
        <li>Switch는 원본 공급자에 1회만 등록</li>
        <li>다른 공급자는 동일 Switch를 참조로 가져와 사용</li>
        <li>SNMP 수집은 원본 등록 기준으로 1회만 수행</li>
      </ul>
    </div>

    <div class="gm-card">
      <h3><i class="fas fa-user-check"></i> 사용자 편의성 고려</h3>
      <p>중복 등록을 막는 것뿐 아니라, 여러 공급자를 함께 관리하는 운영자가 같은 작업을 반복하지 않도록 사용 흐름을 설계했습니다.</p>
      <ul>
        <li>다른 공급자에 이미 등록된 Switch를 목록에서 불러오기만 하면 되어, 동일한 장비 정보를 다시 입력할 필요가 없음</li>
        <li>장비 정보를 반복 입력하지 않으므로 공급자마다 값이 달라지는 입력 실수를 방지</li>
        <li>Switch 정보는 원본 한 곳에서만 관리하면 되어, 참조하는 모든 공급자에 동일하게 반영</li>
        <li>공급자 활성화/비활성화만으로 하위 자원 상태를 일괄 관리하여 자원별 개별 조작 불필요</li>
      </ul>
    </div>
  </div>
</div>

<script>
(function () {
  document.querySelectorAll('#data-center .gm-tab-btn').forEach(function (btn) {
    btn.addEventListener('click', function () {
      document.querySelectorAll('#data-center .gm-tab-btn').forEach(function (b) { b.classList.remove('active'); });
      document.querySelectorAll('#data-center .gm-panel').forEach(function (p) { p.classList.remove('active'); });
      btn.classList.add('active');
      document.getElementById('panel-' + btn.dataset.panel).classList.add('active');
    });
  });
})();
</script>
