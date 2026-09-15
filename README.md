<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PVT — Báo cáo khuyến nghị cổ phiếu | VNDIRECT Research</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,400;8..60,500;8..60,600;8..60,700&family=Inter:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0B0F1A;
    --panel:#111729;
    --panel-2:#0E1424;
    --line:#242C42;
    --line-soft:#1B2138;
    --ink:#E9ECF6;
    --ink-dim:#9AA3C0;
    --ink-faint:#5E6784;
    --orange:#FF6A1A;
    --orange-dim:#FF6A1A33;
    --green:#28C793;
    --green-dim:#28C79322;
    --red:#FF5470;
    --red-dim:#FF547022;
    --gold:#E8B34E;
    --paper:#F5F2EA;
    --paper-ink:#1B1B18;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  body{
    background:var(--bg);
    color:var(--ink);
    font-family:'Inter',sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  ::selection{ background:var(--orange); color:#0B0F1A; }

  .wrap{ max-width:1040px; margin:0 auto; padding:0 28px; }

  /* ---------- MASTHEAD ---------- */
  header.masthead{
    border-bottom:1px solid var(--line);
    padding:22px 0;
    background:linear-gradient(180deg, #0D1120 0%, #0B0F1A 100%);
  }
  .masthead-row{
    display:flex; justify-content:space-between; align-items:flex-end;
    flex-wrap:wrap; gap:14px;
  }
  .wordmark{
    font-family:'Inter',sans-serif; font-weight:700; font-size:15px;
    letter-spacing:0.04em; color:var(--ink);
  }
  .wordmark span{ color:var(--orange); }
  .masthead-meta{
    font-family:'IBM Plex Mono',monospace; font-size:12px; color:var(--ink-faint);
    text-align:right;
  }

  /* ---------- HERO ---------- */
  .hero{ padding:56px 0 40px; border-bottom:1px solid var(--line); }
  .hero-kicker{
    font-family:'IBM Plex Mono',monospace; font-size:12.5px; color:var(--orange);
    margin-bottom:14px;
  }
  .hero-title{
    font-family:'Source Serif 4',serif; font-weight:600;
    font-size:clamp(40px,7vw,64px); line-height:1.02; letter-spacing:-0.01em;
    color:var(--ink); margin-bottom:6px;
  }
  .hero-sub{
    font-family:'Source Serif 4',serif; font-style:italic; font-weight:400;
    font-size:19px; color:var(--ink-dim); max-width:560px; margin-bottom:34px;
  }
  .hero-stats{
    display:grid; grid-template-columns:repeat(4,1fr);
    border-top:1px solid var(--line); border-left:1px solid var(--line);
  }
  .hero-stat{
    border-right:1px solid var(--line); border-bottom:1px solid var(--line);
    padding:18px 20px;
  }
  .hero-stat .label{ font-size:11.5px; color:var(--ink-faint); text-transform:uppercase; letter-spacing:.06em; margin-bottom:8px; }
  .hero-stat .value{ font-family:'IBM Plex Mono',monospace; font-size:24px; font-weight:600; }
  .hero-stat .value.up{ color:var(--green); }
  .hero-stat .value.rate{ color:var(--orange); font-family:'Source Serif 4',serif; font-size:22px;}
  .hero-stat .foot{ font-size:12px; color:var(--ink-faint); margin-top:6px;}

  /* ---------- SECTION GENERIC ---------- */
  section{ padding:52px 0; border-bottom:1px solid var(--line); }
  .sec-head{ display:flex; align-items:baseline; gap:16px; margin-bottom:30px; }
  .sec-num{ font-family:'IBM Plex Mono',monospace; font-size:13px; color:var(--orange); }
  .sec-title{ font-family:'Source Serif 4',serif; font-size:28px; font-weight:600; color:var(--ink); }
  .sec-intro{ font-size:16px; color:var(--ink-dim); max-width:620px; margin-bottom:32px; }

  /* ---------- THESIS LIST ---------- */
  .thesis{ display:flex; flex-direction:column; }
  .thesis-item{
    display:grid; grid-template-columns:64px 1fr; gap:24px;
    padding:26px 0; border-top:1px solid var(--line-soft);
  }
  .thesis-item:last-child{ border-bottom:1px solid var(--line-soft); }
  .thesis-item .n{
    font-family:'Source Serif 4',serif; font-size:34px; color:var(--ink-faint); font-weight:600;
  }
  .thesis-item h3{ font-size:17px; font-weight:600; color:var(--ink); margin-bottom:8px; }
  .thesis-item p{ font-size:14.5px; color:var(--ink-dim); max-width:640px; }
  .thesis-item .tag{
    display:inline-block; font-family:'IBM Plex Mono',monospace; font-size:11px;
    color:var(--green); background:var(--green-dim); padding:3px 8px; border-radius:3px;
    margin-top:10px;
  }

  /* ---------- FINANCE TABLE ---------- */
  table.fin{ width:100%; border-collapse:collapse; font-size:14px; }
  table.fin th{
    text-align:left; font-weight:500; color:var(--ink-faint); font-size:11.5px;
    text-transform:uppercase; letter-spacing:.05em;
    padding:0 14px 12px; border-bottom:1px solid var(--line);
  }
  table.fin td{
    padding:14px; border-bottom:1px solid var(--line-soft);
    font-family:'IBM Plex Mono',monospace; color:var(--ink);
  }
  table.fin td.label{ font-family:'Inter',sans-serif; color:var(--ink-dim); }
  table.fin td.pos{ color:var(--green); }
  table.fin tr:last-child td{ font-weight:600; color:var(--orange); border-bottom:none;}

  /* ---------- RISK ---------- */
  .risk-grid{ display:grid; grid-template-columns:1fr 1fr; gap:1px; background:var(--line); border:1px solid var(--line); }
  .risk-card{ background:var(--panel-2); padding:24px; }
  .risk-card .dot{ width:8px; height:8px; border-radius:50%; background:var(--red); display:inline-block; margin-right:8px;}
  .risk-card h4{ font-size:14.5px; font-weight:600; color:var(--ink); display:inline; }
  .risk-card p{ font-size:13.5px; color:var(--ink-dim); margin-top:10px; }

  /* ---------- CHART HERO PANEL ---------- */
  .chart-section{ padding-top:52px; }
  .terminal{
    background:var(--panel-2); border:1px solid var(--line); border-radius:6px;
    overflow:hidden;
  }
  .terminal-top{
    display:flex; justify-content:space-between; align-items:center;
    padding:16px 20px; border-bottom:1px solid var(--line);
    font-family:'IBM Plex Mono',monospace; font-size:12.5px; color:var(--ink-dim);
  }
  .terminal-top .px{ color:var(--ink); font-size:15px; font-weight:600; }
  .terminal-top .chg{ color:var(--green); margin-left:8px; }
  .chart-canvas-wrap{ padding:20px 16px 8px; }
  .legend-row{
    display:flex; flex-wrap:wrap; gap:18px; padding:14px 20px 20px;
    font-family:'IBM Plex Mono',monospace; font-size:12px; color:var(--ink-dim);
  }
  .legend-row .chip{ display:flex; align-items:center; gap:7px; }
  .legend-row .swatch{ width:14px; height:3px; border-radius:2px; }

  /* ---------- TRADE PLAN ---------- */
  .plan-grid{
    display:grid; grid-template-columns:repeat(4,1fr); gap:1px; background:var(--line);
    border:1px solid var(--line); margin-top:28px;
  }
  .plan-cell{ background:var(--panel-2); padding:22px 20px; }
  .plan-cell .k{ font-size:11.5px; color:var(--ink-faint); text-transform:uppercase; letter-spacing:.05em; margin-bottom:10px;}
  .plan-cell .v{ font-family:'IBM Plex Mono',monospace; font-size:21px; font-weight:600; color:var(--ink); }
  .plan-cell.buy .v{ color:var(--green); }
  .plan-cell.tp .v{ color:var(--orange); }
  .plan-cell.sl .v{ color:var(--red); }
  .plan-cell .note{ font-size:12px; color:var(--ink-faint); margin-top:8px; }

  /* ---------- DISCLAIMER / FOOTER ---------- */
  footer{ padding:40px 0 60px; }
  .disclaimer{
    background:var(--panel); border-left:2px solid var(--orange);
    padding:20px 24px; font-size:12.5px; color:var(--ink-dim); line-height:1.7;
  }
  .foot-meta{
    display:flex; justify-content:space-between; margin-top:28px;
    font-family:'IBM Plex Mono',monospace; font-size:11.5px; color:var(--ink-faint);
    flex-wrap:wrap; gap:10px;
  }

  @media (max-width:720px){
    .hero-stats{ grid-template-columns:1fr 1fr; }
    .thesis-item{ grid-template-columns:40px 1fr; gap:14px; }
    .risk-grid{ grid-template-columns:1fr; }
    .plan-grid{ grid-template-columns:1fr 1fr; }
    .hero-title{ font-size:38px; }
  }
</style>
</head>
<body>

<header class="masthead">
  <div class="wrap masthead-row">
    <div class="wordmark">VN<span>DIRECT</span> RESEARCH</div>
    <div class="masthead-meta">BÁO CÁO NỘI BỘ · PHÒNG DVCK39<br>Cập nhật: 16/09/2026</div>
  </div>
</header>

<section class="hero">
  <div class="wrap">
    <div class="hero-kicker">CỔ PHIẾU NGÀNH VẬN TẢI DẦU KHÍ · HOSE</div>
    <div class="hero-title">PVT</div>
    <p class="hero-sub">Đội tàu mở rộng, giá cước leo thang — PVTrans bước vào chu kỳ lợi nhuận kỷ lục nhờ căng thẳng Trung Đông và chiến lược liên minh vận tải quốc tế.</p>

    <div class="hero-stats">
      <div class="hero-stat">
        <div class="label">Giá hiện tại</div>
        <div class="value">22.650</div>
        <div class="foot">VNĐ/CP · 15/09/2026</div>
      </div>
      <div class="hero-stat">
        <div class="label">Khuyến nghị</div>
        <div class="value rate">KHẢ QUAN</div>
        <div class="foot">Trung hạn 6–12 tháng</div>
      </div>
      <div class="hero-stat">
        <div class="label">Giá mục tiêu</div>
        <div class="value up">25.000 – 27.800</div>
        <div class="foot">Upside ~10 – 23%</div>
      </div>
      <div class="hero-stat">
        <div class="label">P/E dự phóng 2026</div>
        <div class="value">~8,3x</div>
        <div class="foot">Thấp hơn TB ngành (~10x)</div>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="sec-head"><span class="sec-num">01</span><span class="sec-title">Luận điểm đầu tư</span></div>
    <p class="sec-intro">Ba động lực đang hội tụ cùng lúc, đưa PVTrans bước vào giai đoạn lợi nhuận tốt nhất trong nhiều năm trở lại đây.</p>

    <div class="thesis">
      <div class="thesis-item">
        <div class="n">01</div>
        <div>
          <h3>Giá cước vận tải biển leo thang vì căng thẳng Trung Đông</h3>
          <p>Quý 2/2026, giá thuê ngày bình quân tàu chở sản phẩm dầu tăng tới 160% so với cùng kỳ và 53,9% so với quý trước; giá thuê tàu chở dầu thô tăng tương ứng 142,3% và 18,1%. Xung đột địa chính trị làm gián đoạn nguồn cung tàu, đẩy phí bảo hiểm rủi ro chiến tranh lên cao và khiến chủ tàu thận trọng hơn — thu hẹp nguồn cung đội tàu hoạt động toàn cầu.</p>
          <span class="tag">Giá thuê tàu +142% ~ +160% YoY</span>
        </div>
      </div>
      <div class="thesis-item">
        <div class="n">02</div>
        <div>
          <h3>Mở rộng đội tàu, tham gia liên minh vận tải quốc tế</h3>
          <p>Khoảng 30% đội tàu chở dầu của PVTrans hiện tham gia các liên minh đội tàu quốc tế, tận dụng đà tăng giá trên thị trường giao ngay. Quy mô đội tàu dự kiến tăng từ 64 chiếc (2025) lên 71 chiếc (2026) và 76 chiếc (2027), tổng trọng tải tăng từ 1,97 triệu DWT lên 2,34 triệu DWT.</p>
          <span class="tag">Đội tàu +12 chiếc trong 2 năm</span>
        </div>
      </div>
      <div class="thesis-item">
        <div class="n">03</div>
        <div>
          <h3>Chuyển dịch sang hợp đồng dài hạn, khóa lợi nhuận cao</h3>
          <p>Từ nửa cuối 2026 đến 2027, PVTrans chuyển dần sang các hợp đồng thuê tàu dài hạn 1–2 năm thay vì phụ thuộc thị trường giao ngay. Mặt bằng giá tái ký hiện cao hơn khoảng 35% so với cùng kỳ — giúp doanh nghiệp ổn định dòng tiền cho giai đoạn tới thay vì chỉ hưởng lợi ngắn hạn.</p>
          <span class="tag">Giá tái ký hợp đồng +35% YoY</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="sec-head"><span class="sec-num">02</span><span class="sec-title">Kết quả kinh doanh</span></div>
    <p class="sec-intro">Lợi nhuận quý 2/2026 lập kỷ lục — 6 tháng đầu năm đã hoàn thành gần 90% kế hoạch lợi nhuận cả năm.</p>

    <table class="fin">
      <thead>
        <tr><th>Chỉ tiêu</th><th>Quý 2/2026</th><th>% YoY</th><th>6 tháng 2026</th><th>% YoY</th></tr>
      </thead>
      <tbody>
        <tr>
          <td class="label">Doanh thu thuần</td>
          <td>5.714 tỷ</td><td class="pos">+32,5%</td>
          <td>9.754 tỷ</td><td class="pos">+37,3%</td>
        </tr>
        <tr>
          <td class="label">Lợi nhuận trước thuế</td>
          <td>834 tỷ</td><td class="pos">+91,2%</td>
          <td>1.366 tỷ</td><td class="pos">+75,0%</td>
        </tr>
        <tr>
          <td class="label">LNST cổ đông công ty mẹ</td>
          <td>553 tỷ (kỷ lục)</td><td class="pos">+87,6%</td>
          <td>1.094 tỷ*</td><td class="pos">+71,7%</td>
        </tr>
        <tr>
          <td class="label">Dự phóng cả năm 2026</td>
          <td colspan="4">Doanh thu ~20.914 tỷ (+30% YoY) · LNTT ~2.834 tỷ (+71% YoY)</td>
        </tr>
      </tbody>
    </table>
    <p style="font-size:12px;color:var(--ink-faint);margin-top:14px;">* LNST hợp nhất toàn công ty 6 tháng 2026.</p>
  </div>
</section>

<section>
  <div class="wrap">
    <div class="sec-head"><span class="sec-num">03</span><span class="sec-title">Rủi ro cần lưu ý</span></div>
    <p class="sec-intro">Câu chuyện tăng trưởng hiện tại gắn chặt với yếu tố địa chính trị — nhà đầu tư cần theo dõi sát khả năng đảo chiều của chu kỳ giá cước.</p>

    <div class="risk-grid">
      <div class="risk-card">
        <span class="dot"></span><h4>Giá cước có thể hạ nhiệt</h4>
        <p>Nếu vận tải qua eo biển Hormuz trở lại bình thường và tốc độ tăng đội tàu toàn cầu vượt tăng trưởng nhu cầu, giá cước có thể giảm khoảng 30% so với mức nền cao hiện tại trong kịch bản cơ sở.</p>
      </div>
      <div class="risk-card">
        <span class="dot"></span><h4>Chi phí mở rộng đội tàu tăng vọt</h4>
        <p>Giá tàu cũ đã tăng 20–60% chỉ trong một năm. PVT phải hạ mục tiêu mua tàu mới 2026 xuống còn 4 chiếc, chưa hoàn tất thương vụ nào trong nửa đầu năm dù đã được ĐHCĐ thông qua.</p>
      </div>
      <div class="risk-card">
        <span class="dot"></span><h4>Tăng trưởng nhu cầu vận tải hạn chế</h4>
        <p>Dù quãng đường vận chuyển dài hơn do nguồn cung dầu dịch chuyển sang Mỹ/Brazil, lượng bổ sung chưa đủ bù đắp sản lượng sụt giảm từ Trung Đông.</p>
      </div>
      <div class="risk-card">
        <span class="dot"></span><h4>Định giá đã phản ánh một phần kỳ vọng</h4>
        <p>Giá cổ phiếu đã tăng mạnh từ vùng 17–20 lên 22,65 — phần lớn tin tốt về KQKD kỷ lục quý 2 đã được thị trường ghi nhận vào giá.</p>
      </div>
    </div>
  </div>
</section>

<section class="chart-section">
  <div class="wrap">
    <div class="sec-head"><span class="sec-num">04</span><span class="sec-title">Biểu đồ kỹ thuật &amp; kế hoạch giao dịch</span></div>
    <p class="sec-intro">Giá đã bứt phá khỏi vùng tích lũy tháng 8 và test lại vùng đỉnh cũ tháng 6 — cấu trúc kỹ thuật đang ủng hộ xu hướng phục hồi ngắn hạn.</p>

    <div class="terminal">
      <div class="terminal-top">
        <div>PVT · 1D · HOSE</div>
        <div><span class="px">22.650</span><span class="chg">▲ +0,22%</span></div>
      </div>
      <div class="chart-canvas-wrap">
        <canvas id="pvtChart" height="360"></canvas>
      </div>
      <div class="legend-row">
        <div class="chip"><span class="swatch" style="background:#28C793"></span>Vùng mua tích lũy</div>
        <div class="chip"><span class="swatch" style="background:#FF6A1A"></span>Mục tiêu 1 — 25.000</div>
        <div class="chip"><span class="swatch" style="background:#E8B34E"></span>Mục tiêu 2 — 27.800</div>
        <div class="chip"><span class="swatch" style="background:#FF5470"></span>Dừng lỗ — 19.500</div>
      </div>
    </div>

    <div class="plan-grid">
      <div class="plan-cell buy">
        <div class="k">Vùng mua</div>
        <div class="v">20.500–21.500</div>
        <div class="note">Giải ngân khi giá điều chỉnh về vùng nền giá cũ</div>
      </div>
      <div class="plan-cell tp">
        <div class="k">Chốt lời 1</div>
        <div class="v">25.000</div>
        <div class="note">Upside ~10% · vùng đỉnh cũ tháng 6</div>
      </div>
      <div class="plan-cell tp">
        <div class="k">Chốt lời 2</div>
        <div class="v">27.800</div>
        <div class="note">Upside ~23% · kịch bản KQKD vượt kế hoạch</div>
      </div>
      <div class="plan-cell sl">
        <div class="k">Dừng lỗ</div>
        <div class="v">19.500</div>
        <div class="note">Nếu mất vùng hỗ trợ nền giá, xu hướng tăng bị phá vỡ</div>
      </div>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div class="disclaimer">
      <strong style="color:var(--ink)">Khuyến cáo:</strong> Báo cáo này được tổng hợp cho mục đích tham khảo nội bộ, dựa trên số liệu công bố công khai và phân tích kỹ thuật tại thời điểm phát hành. Đây không phải cam kết lợi nhuận hay khuyến nghị mua/bán mang tính chỉ dẫn tuyệt đối. Nhà đầu tư cần đối chiếu với diễn biến thị trường thời gian thực và khẩu vị rủi ro cá nhân trước khi ra quyết định giao dịch.
    </div>
    <div class="foot-meta">
      <span>VNDIRECT SECURITIES · PHÒNG DVCK39</span>
      <span>Báo cáo phát hành nội bộ — không phổ biến ngoài phạm vi tư vấn khách hàng</span>
    </div>
  </div>
</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.4/chart.umd.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/chartjs-plugin-annotation/3.0.1/chartjs-plugin-annotation.min.js"></script>
<script>
const labels = ['T11','','T12','','T1','','T2','','','T3','','T4','','T5','','T6','','T7','','T8','','T9-a','T9-b','Hiện tại'];
const prices = [16.5,17.0,16.8,17.5,18.0,19.8,24.0,29.3,25.5,23.0,21.5,21.0,22.3,21.8,22.6,21.5,20.8,21.2,19.5,17.3,17.8,19.0,20.45,22.65];

const ctx = document.getElementById('pvtChart').getContext('2d');
const grad = ctx.createLinearGradient(0,0,0,340);
grad.addColorStop(0,'rgba(255,106,26,0.28)');
grad.addColorStop(1,'rgba(255,106,26,0.0)');

new Chart(ctx, {
  type: 'line',
  data: {
    labels: labels,
    datasets: [{
      data: prices,
      borderColor: '#FF6A1A',
      backgroundColor: grad,
      borderWidth: 2,
      fill: true,
      tension: 0.35,
      pointRadius: 0,
      pointHoverRadius: 5,
      pointHoverBackgroundColor: '#FF6A1A',
      pointHitRadius: 12
    }]
  },
  options: {
    responsive: true,
    interaction: { mode: 'index', intersect: false },
    scales: {
      x: {
        grid: { color: '#1B2138', drawTicks:false },
        ticks: { color: '#5E6784', font:{ family:'IBM Plex Mono', size:11 } },
        border: { color:'#242C42' }
      },
      y: {
        min: 14, max: 31,
        grid: { color: '#1B2138' },
        ticks: { color: '#5E6784', font:{ family:'IBM Plex Mono', size:11 }, callback:(v)=>v.toFixed(1) },
        border: { color:'#242C42' }
      }
    },
    plugins: {
      legend: { display:false },
      tooltip: {
        backgroundColor:'#0E1424',
        borderColor:'#242C42',
        borderWidth:1,
        titleFont:{ family:'IBM Plex Mono', size:11 },
        bodyFont:{ family:'IBM Plex Mono', size:12 },
        padding:10,
        callbacks:{ label:(c)=> ' ' + c.parsed.y.toFixed(2) + ' nghìn đồng' }
      },
      annotation: {
        annotations: {
          buyZone: {
            type: 'box',
            yMin: 20.5, yMax: 21.5,
            backgroundColor: 'rgba(40,199,147,0.10)',
            borderColor: 'rgba(40,199,147,0.5)',
            borderWidth: 1,
            borderDash: [4,3],
            label: {
              display: true, content: 'VÙNG MUA', position: 'start',
              color:'#28C793', font:{ family:'IBM Plex Mono', size:10, weight:'600'},
              backgroundColor:'rgba(11,15,26,0.85)', padding:4
            }
          },
          tp1: {
            type: 'line', yMin: 25.0, yMax: 25.0,
            borderColor: '#FF6A1A', borderWidth: 1.5, borderDash: [6,4],
            label: {
              display:true, content:'TP1 · 25.000', position:'end',
              color:'#FF6A1A', font:{ family:'IBM Plex Mono', size:10, weight:'600'},
              backgroundColor:'rgba(11,15,26,0.85)', padding:4
            }
          },
          tp2: {
            type: 'line', yMin: 27.8, yMax: 27.8,
            borderColor: '#E8B34E', borderWidth: 1.5, borderDash: [6,4],
            label: {
              display:true, content:'TP2 · 27.800', position:'end',
              color:'#E8B34E', font:{ family:'IBM Plex Mono', size:10, weight:'600'},
              backgroundColor:'rgba(11,15,26,0.85)', padding:4
            }
          },
          sl: {
            type: 'line', yMin: 19.5, yMax: 19.5,
            borderColor: '#FF5470', borderWidth: 1.5, borderDash: [6,4],
            label: {
              display:true, content:'SL · 19.500', position:'end',
              color:'#FF5470', font:{ family:'IBM Plex Mono', size:10, weight:'600'},
              backgroundColor:'rgba(11,15,26,0.85)', padding:4
            }
          },
          current: {
            type: 'point',
            xValue: 23, yValue: 22.65,
            backgroundColor: '#FF6A1A',
            borderColor: '#0B0F1A',
            borderWidth: 2,
            radius: 5
          }
        }
      }
    }
  }
});
</script>

</body>
</html>
