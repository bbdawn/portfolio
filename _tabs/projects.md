---
layout: page
title: Projects
icon: fas fa-folder-open
order: 1
permalink: /projects/
---

<style>
  .pj-card {
    display: block; border: 1px solid var(--main-border-color, #e0e0e0);
    border-radius: 10px; padding: 1.1rem 1.25rem; text-decoration: none !important;
    color: inherit; transition: border-color 0.15s, transform 0.15s; margin-bottom: 0.9rem;
  }
  .pj-card:hover { border-color: var(--link-color); transform: translateY(-1px); }
  .pj-card .pj-title { font-size: 1rem; font-weight: 700; margin-bottom: 0.35rem; display: flex; align-items: center; gap: 0.45rem; }
  .pj-card .pj-title i { color: var(--link-color); opacity: 0.85; }
  .pj-card .pj-desc { font-size: 0.88rem; line-height: 1.65; opacity: 0.7; }
</style>

<a class="pj-card" href="{{ '/gpu-manager/' | relative_url }}">
  <div class="pj-title"><i class="fas fa-toolbox"></i> GPU Manager</div>
  <div class="pj-desc">수동 10분 걸리던 GPU mdev 판단 작업을, 도구화해서 비전문가도 바로 처리할 수 있게 만든 과정</div>
</a>

<a class="pj-card" href="{{ site.baseurl }}{% post_url 2026-06-30-octavia-ssl-offloading %}">
  <div class="pj-title"><i class="fas fa-lock"></i> Octavia SSL Offloading</div>
  <div class="pj-desc">Octavia 로드밸런서에 TERMINATED_HTTPS 리스너와 Barbican 인증서 연동을 붙여 SSL Offloading 기능을 구현한 과정</div>
</a>

<a class="pj-card" href="{{ site.baseurl }}{% post_url 2026-06-30-rack-topology %}">
  <div class="pj-title"><i class="fas fa-server"></i> 데이터센터 Rack Topology</div>
  <div class="pj-desc">DB 설계부터 API까지 직접 구현한 데이터센터 랙/자원 시각화 프로젝트 — OpenStack 연동 가상 네트워크 토폴로지, 물리 네트워크 토폴로지 기능 포함</div>
</a>
