<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SME Profit Sharing Proposal</title>
    <!-- Fonts & Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Pretendard:wght@100..900&family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --primary: #0ea5e9;
            --secondary: #6366f1;
            --bg-dark: #020617;
            --surface: #0f172a;
        }

        body {
            font-family: 'Pretendard', sans-serif;
            background-color: var(--bg-dark);
            color: #f1f5f9;
            overflow: hidden; /* Prevent scrolling for the presentation feel */
        }

        .slide {
            display: none;
            height: 100vh;
            width: 100vw;
            padding: 4rem;
            animation: fadeIn 0.5s ease-out forwards;
        }

        .slide.active {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .gradient-text {
            background: linear-gradient(135deg, #f8fafc 0%, #94a3b8 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .card {
            background: rgba(30, 41, 59, 0.5);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 1.5rem;
            padding: 2rem;
            transition: all 0.3s ease;
        }

        .card:hover {
            border-color: var(--primary);
            background: rgba(30, 41, 59, 0.8);
        }

        .progress-bar {
            position: fixed;
            bottom: 0;
            left: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            transition: width 0.3s ease;
            z-index: 50;
        }

        .nav-btn {
            background: rgba(30, 41, 59, 0.8);
            border: 1px solid rgba(255, 255, 255, 0.1);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.2s;
        }

        .nav-btn:hover {
            background: var(--primary);
            transform: scale(1.1);
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .slide { padding: 2rem; }
            h1 { font-size: 2.5rem !important; }
        }
    </style>
</head>
<body>

    <!-- Progress Bar -->
    <div id="progress" class="progress-bar" style="width: 0%"></div>

    <!-- Navigation Controls -->
    <div class="fixed bottom-8 right-8 flex gap-4 z-50">
        <button onclick="prevSlide()" class="nav-btn" title="이전 슬라이드 (Left Arrow)">
            <i class="fas fa-chevron-left"></i>
        </button>
        <div class="flex items-center justify-center bg-slate-800 px-4 rounded-full text-sm font-medium border border-slate-700">
            <span id="slide-number">1</span> / <span id="total-slides">12</span>
        </div>
        <button onclick="nextSlide()" class="nav-btn" title="다음 슬라이드 (Right Arrow / Space)">
            <i class="fas fa-chevron-right"></i>
        </button>
    </div>

    <!-- Slides Container -->
    <main id="presentation">
        
        <!-- Slide 1: Title -->
        <section class="slide active" id="slide-1">
            <div class="max-w-6xl mx-auto text-center">
                <span class="inline-block px-4 py-1 mb-6 text-sm font-bold tracking-widest text-sky-400 uppercase border border-sky-400/30 rounded-full">STRATEGIC PROPOSAL</span>
                <h1 class="text-6xl md:text-8xl font-black mb-8 leading-tight gradient-text">
                    중소기업 성과공유제<br>도입 제안
                </h1>
                <p class="text-xl md:text-2xl text-slate-400 max-w-3xl mx-auto">
                    인재 확보 및 절세를 통한 우리 회사의 새로운 성장 동력 확보 방안
                </p>
                <div class="mt-12 flex justify-center gap-4 text-slate-500 font-medium">
                    <span>전략기획팀</span>
                    <span>|</span>
                    <span>2024. 05. 22</span>
                </div>
            </div>
        </section>

        <!-- Slide 2: Definition -->
        <section class="slide" id="slide-2">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6">01. 성과공유제의 정의</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <div class="card">
                        <h3 class="text-2xl font-bold text-sky-400 mb-4">제도 개요</h3>
                        <p class="text-slate-300 leading-relaxed text-lg">
                            중소기업과 근로자가 성과를 공유하고 있거나 공유하기로 약정한 기업을 의미합니다. 
                            <strong>'중소기업 인력지원 특별법'</strong>에 근거한 정부 공식 인증 제도입니다.
                        </p>
                    </div>
                    <div class="card">
                        <h3 class="text-2xl font-bold text-sky-400 mb-4">핵심 목적</h3>
                        <ul class="space-y-3 text-slate-300">
                            <li><i class="fas fa-check text-sky-500 mr-2"></i> 우수 인력의 장기 재직 유도</li>
                            <li><i class="fas fa-check text-sky-500 mr-2"></i> 기업 생산성 향상 및 경쟁력 강화</li>
                            <li><i class="fas fa-check text-sky-500 mr-2"></i> 정부 정책 지원 및 세제 혜택 수혜</li>
                        </ul>
                    </div>
                </div>
                <div class="rounded-3xl overflow-hidden shadow-2xl border border-slate-700 h-[400px]">
                    <!--  -->
                    <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=800&q=80" alt="Team Work" class="w-full h-full object-cover">
                </div>
            </div>
        </section>

        <!-- Slide 3: 7 Types -->
        <section class="slide" id="slide-3">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6 text-center">성과공유의 7가지 유형</h2>
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
                <div class="card text-center">
                    <i class="fas fa-money-bill-trend-up text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">성과급 지급</h4>
                    <p class="text-sm text-slate-400">경영목표 달성 시 지급</p>
                </div>
                <div class="card text-center border-sky-500/50">
                    <i class="fas fa-piggy-bank text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">성과보상공제</h4>
                    <p class="text-sm text-slate-400">내일채움공제 등 출연</p>
                </div>
                <div class="card text-center">
                    <i class="fas fa-chart-pie text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">우리사주/옵션</h4>
                    <p class="text-sm text-slate-400">주식매수선택권 부여</p>
                </div>
                <div class="card text-center">
                    <i class="fas fa-arrow-up-right-dots text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">임금 상승</h4>
                    <p class="text-sm text-slate-400">평균 임금 상승률 이상</p>
                </div>
                <div class="card text-center">
                    <i class="fas fa-hospital-user text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">사내복지기금</h4>
                    <p class="text-sm text-slate-400">복지기금 설치 및 운영</p>
                </div>
                <div class="card text-center">
                    <i class="fas fa-user-graduate text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">인재육성인증</h4>
                    <p class="text-sm text-slate-400">중기부 인재육성 기업</p>
                </div>
                <div class="card text-center">
                    <i class="fas fa-users-viewfinder text-4xl text-sky-400 mb-4"></i>
                    <h4 class="font-bold mb-2 text-xl">기타 인증</h4>
                    <p class="text-sm text-slate-400">가족친화인증 등 포함</p>
                </div>
                <div class="card bg-sky-500/10 border-sky-500 flex items-center justify-center">
                    <p class="font-bold text-sky-400">우리 회사 맞춤형 설계 가능</p>
                </div>
            </div>
        </section>

        <!-- Slide 4: Business Benefits -->
        <section class="slide" id="slide-4">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6">02. 기업을 위한 정책 지원</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="card flex gap-6 items-start">
                    <div class="bg-sky-500/20 p-4 rounded-2xl text-sky-400">
                        <i class="fas fa-building-columns text-2xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xl font-bold mb-2">정책자금 우대</h4>
                        <p class="text-slate-400">중진공 정책자금 융자 한도 확대 및 심사 가점 부여</p>
                    </div>
                </div>
                <div class="card flex gap-6 items-start">
                    <div class="bg-indigo-500/20 p-4 rounded-2xl text-indigo-400">
                        <i class="fas fa-award text-2xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xl font-bold mb-2">정부 사업 가점</h4>
                        <p class="text-slate-400">R&D 지원사업, 수출 바우처 사업 참여 시 우대 가점</p>
                    </div>
                </div>
                <div class="card flex gap-6 items-start border-emerald-500/30">
                    <div class="bg-emerald-500/20 p-4 rounded-2xl text-emerald-400">
                        <i class="fas fa-user-shield text-2xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xl font-bold mb-2">병역지정업체 선정</h4>
                        <p class="text-slate-400">산업기능요원 인력 배정 시 필수적인 높은 가점(최대 4점)</p>
                    </div>
                </div>
                <div class="card flex gap-6 items-start">
                    <div class="bg-amber-500/20 p-4 rounded-2xl text-amber-400">
                        <i class="fas fa-star text-2xl"></i>
                    </div>
                    <div>
                        <h4 class="text-xl font-bold mb-2">기업 브랜드 강화</h4>
                        <p class="text-slate-400">'성과공유 인증 마크' 활용으로 채용 시장 내 경쟁력 우위</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Slide 5: Military Service Points -->
        <section class="slide" id="slide-5">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6">병역지정업체 선정 가점 (상세)</h2>
            <div class="overflow-hidden rounded-3xl border border-slate-800 bg-slate-900/50">
                <table class="w-full text-left">
                    <thead class="bg-slate-800/50">
                        <tr>
                            <th class="p-6 text-sky-400">구분</th>
                            <th class="p-6 text-sky-400">도입 수준</th>
                            <th class="p-6 text-sky-400 text-center">누적 가점</th>
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-slate-800">
                        <tr>
                            <td class="p-6 font-bold">1단계 (도약)</td>
                            <td class="p-6">성과공유 유형 1개 도입 기업</td>
                            <td class="p-6 text-center text-xl font-bold">1점</td>
                        </tr>
                        <tr>
                            <td class="p-6 font-bold">2단계 (우수)</td>
                            <td class="p-6">성과공유 유형 2~3개 도입 기업</td>
                            <td class="p-6 text-center text-xl font-bold">2~3점</td>
                        </tr>
                        <tr class="bg-sky-500/5">
                            <td class="p-6 font-bold text-sky-400">3단계 (으뜸)</td>
                            <td class="p-6">다수 유형 도입 및 성과공유 모범 기업</td>
                            <td class="p-6 text-center text-2xl font-bold text-sky-400">4점 이상</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <p class="mt-8 text-slate-500 text-center italic">※ 병역특례 업체 지정은 우리 회사 기술 인력 수급의 핵심 열쇠입니다.</p>
        </section>

        <!-- Slide 6: Tax Incentive Enterprise -->
        <section class="slide" id="slide-6">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6">03. 강력한 세제 지원 (기업)</h2>
            <div class="flex flex-col md:flex-row items-center gap-12">
                <div class="flex-1 text-center">
                    <div class="inline-flex flex-col items-center justify-center w-64 h-64 rounded-full bg-sky-500/10 border-4 border-sky-500 shadow-[0_0_50px_rgba(14,165,233,0.3)]">
                        <span class="text-8xl font-black text-sky-400">10<span class="text-4xl">%</span></span>
                        <span class="text-lg font-bold text-slate-300">세액 공제</span>
                    </div>
                </div>
                <div class="flex-[1.5] space-y-8">
                    <div class="card bg-slate-800/80">
                        <h4 class="text-2xl font-bold mb-4">법인세/소득세 직접 공제</h4>
                        <p class="text-lg text-slate-300 leading-relaxed">
                            근로자에게 지급한 성과급의 <strong>10%를 해당 연도 법인세에서 감면</strong>받습니다. 
                            단순 경비 처리가 아닌 '세액 공제'이므로 실질적인 현금 확보 효과가 큽니다.
                        </p>
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div class="p-4 bg-slate-900 rounded-xl border border-slate-700 text-center">
                            <span class="block text-slate-500 text-sm mb-1">절세 항목</span>
                            <span class="font-bold">법인세</span>
                        </div>
                        <div class="p-4 bg-slate-900 rounded-xl border border-slate-700 text-center">
                            <span class="block text-slate-500 text-sm mb-1">공제 대상</span>
                            <span class="font-bold">지급 성과급 전체</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Slide 7: Tax Incentive Employee -->
        <section class="slide" id="slide-7">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-emerald-500 pl-6">04. 강력한 세제 지원 (근로자)</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <div class="card border-emerald-500/30 bg-emerald-500/5">
                    <div class="flex items-center gap-4 mb-6">
                        <div class="w-16 h-16 rounded-2xl bg-emerald-500 flex items-center justify-center text-white text-3xl">
                            <i class="fas fa-user-check"></i>
                        </div>
                        <h3 class="text-3xl font-bold">근로자 혜택</h3>
                    </div>
                    <p class="text-xl text-slate-300 mb-8">
                        성과급 수령 시 발생하는 추가 소득세에 대해 <br>
                        <span class="text-4xl font-black text-emerald-400">50% 세액 감면</span>
                    </p>
                    <ul class="space-y-4 text-slate-400">
                        <li><i class="fas fa-check text-emerald-500 mr-2"></i> 실질 소득(실수령액) 증대 효과</li>
                        <li><i class="fas fa-check text-emerald-500 mr-2"></i> 대기업과의 임금 격차 완화</li>
                        <li><i class="fas fa-check text-emerald-500 mr-2"></i> 핵심 인력 장기 근속 동기 부여</li>
                    </ul>
                </div>
                <div class="flex flex-col justify-center">
                    <div class="bg-slate-800/50 p-8 rounded-3xl border border-slate-700">
                        <h4 class="text-xl font-bold mb-4 text-sky-400">성과공유의 시너지</h4>
                        <div class="space-y-6">
                            <div class="flex justify-between items-center p-4 bg-slate-900/50 rounded-xl">
                                <span>회사</span>
                                <i class="fas fa-arrow-right text-slate-500"></i>
                                <span class="font-bold text-sky-400">법인세 10% 절감</span>
                            </div>
                            <div class="flex justify-between items-center p-4 bg-slate-900/50 rounded-xl">
                                <span>직원</span>
                                <i class="fas fa-arrow-right text-slate-500"></i>
                                <span class="font-bold text-emerald-400">소득세 50% 절감</span>
                            </div>
                        </div>
                        <p class="mt-6 text-sm text-slate-500 text-center">정부 재원으로 노사가 함께 상생하는 최고의 카드입니다.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Slide 8: Requirements -->
        <section class="slide" id="slide-8">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6 text-center">도입 및 유지 요건</h2>
            <div class="max-w-4xl mx-auto space-y-6">
                <div class="card flex gap-8 items-center border-l-4 border-l-sky-500">
                    <div class="text-5xl font-black text-slate-800">01</div>
                    <div>
                        <h4 class="text-xl font-bold">임금 수준 유지</h4>
                        <p class="text-slate-400">1인당 연간 임금 총액(성과급 제외)이 전년보다 감소하지 않아야 함</p>
                    </div>
                </div>
                <div class="card flex gap-8 items-center border-l-4 border-l-sky-500">
                    <div class="text-5xl font-black text-slate-800">02</div>
                    <div>
                        <h4 class="text-xl font-bold">최소 지급 기준</h4>
                        <p class="text-slate-400">대상 근로자 1인당 연간 <strong>35만원 이상</strong> 지급 또는 출연</p>
                    </div>
                </div>
                <div class="card flex gap-8 items-center border-l-4 border-l-sky-500">
                    <div class="text-5xl font-black text-slate-800">03</div>
                    <div>
                        <h4 class="text-xl font-bold">사전 서면 약정</h4>
                        <p class="text-slate-400">경영목표 및 보상 방식에 대해 사전에 직원과 서면으로 합의</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Slide 9: Implementation Roadmap -->
        <section class="slide" id="slide-9">
            <h2 class="text-4xl font-bold mb-12 border-l-8 border-sky-500 pl-6 text-center">도입 로드맵</h2>
            <div class="relative max-w-5xl mx-auto py-10">
                <div class="absolute top-1/2 left-0 w-full h-1 bg-slate-800 -translate-y-1/2 hidden md:block"></div>
                <div class="grid grid-cols-1 md:grid-cols-4 gap-8 relative z-10">
                    <div class="text-center">
                        <div class="w-12 h-12 bg-sky-500 rounded-full flex items-center justify-center mx-auto mb-4 font-bold text-lg">1</div>
                        <h5 class="font-bold mb-2">현황 진단</h5>
                        <p class="text-xs text-slate-500">우리사 성과급<br>구조 파악</p>
                    </div>
                    <div class="text-center">
                        <div class="w-12 h-12 bg-sky-500 rounded-full flex items-center justify-center mx-auto mb-4 font-bold text-lg">2</div>
                        <h5 class="font-bold mb-2">제도 설계</h5>
                        <p class="text-xs text-slate-500">유형 선택 및<br>지급 기준 설정</p>
                    </div>
                    <div class="text-center">
                        <div class="w-12 h-12 bg-sky-500 rounded-full flex items-center justify-center mx-auto mb-4 font-bold text-lg">3</div>
                        <h5 class="font-bold mb-2">서면 약정</h5>
                        <p class="text-xs text-slate-500">근로자 동의 및<br>계약 체결</p>
                    </div>
                    <div class="text-center">
                        <div class="w-12 h-12 bg-emerald-500 rounded-full flex items-center justify-center mx-auto mb-4 font-bold text-lg"><i class="fas fa-check"></i></div>
                        <h5 class="font-bold mb-2">인증 등록</h5>
                        <p class="text-xs text-slate-500">산인공 온라인<br>등록 및 승인</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Slide 10: Conclusion -->
        <section class="slide" id="slide-10">
            <div class="max-w-4xl mx-auto text-center space-y-12">
                <h2 class="text-5xl font-black gradient-text">성공적인 인재 경영의<br>첫 걸음입니다.</h2>
                <div class="grid grid-cols-3 gap-8">
                    <div>
                        <span class="block text-4xl font-bold text-sky-400 mb-2">Save</span>
                        <p class="text-slate-400">기업 법인세 10%<br>즉시 공제</p>
                    </div>
                    <div>
                        <span class="block text-4xl font-bold text-emerald-400 mb-2">Keep</span>
                        <p class="text-slate-400">우수 핵심 인력<br>이탈 방지</p>
                    </div>
                    <div>
                        <span class="block text-4xl font-bold text-indigo-400 mb-2">Get</span>
                        <p class="text-slate-400">정부 지원 사업<br>우선권 확보</p>
                    </div>
                </div>
                <p class="text-2xl text-slate-300 font-medium pt-12">
                    "성과를 나누면, 성장이 따라옵니다."
                </p>
            </div>
        </section>

        <!-- Slide 11: Q&A -->
        <section class="slide" id="slide-11">
            <div class="text-center">
                <h1 class="text-9xl font-black text-slate-800 mb-8">Q&A</h1>
                <p class="text-3xl font-bold mb-12">경청해 주셔서 감사합니다.</p>
                <p class="text-slate-500">본 도입 제안에 대한 질의응답을 진행하겠습니다.</p>
            </div>
        </section>

        <!-- Slide 12: Contact -->
        <section class="slide" id="slide-12">
            <div class="max-w-2xl mx-auto card text-center">
                <h3 class="text-3xl font-bold mb-8 text-sky-400">NEXT STEP</h3>
                <p class="text-lg text-slate-300 mb-12 leading-relaxed">
                    승인 시, 즉각적인 시뮬레이션을 통해 <br>
                    우리 회사의 **예상 절세액**과 **도입 비용**에 대한 <br>
                    상세 보고서를 1주일 내로 제출하겠습니다.
                </p>
                <button onclick="goToSlide(1)" class="bg-sky-500 hover:bg-sky-600 text-white font-bold py-4 px-10 rounded-full transition-all shadow-lg shadow-sky-500/20">
                    첫 화면으로 돌아가기
                </button>
            </div>
        </section>

    </main>

    <script>
        let currentSlide = 1;
        const totalSlides = 12;

        function updateSlide() {
            // Hide all slides
            document.querySelectorAll('.slide').forEach(s => s.classList.remove('active'));
            // Show current
            document.getElementById(`slide-${currentSlide}`).classList.add('active');
            
            // Update UI
            document.getElementById('slide-number').innerText = currentSlide;
            const progress = ((currentSlide - 1) / (totalSlides - 1)) * 100;
            document.getElementById('progress').style.width = `${progress}%`;
            
            // Reset scroll to top of slide
            window.scrollTo(0,0);
        }

        function nextSlide() {
            if (currentSlide < totalSlides) {
                currentSlide++;
                updateSlide();
            }
        }

        function prevSlide() {
            if (currentSlide > 1) {
                currentSlide--;
                updateSlide();
            }
        }

        function goToSlide(n) {
            currentSlide = n;
            updateSlide();
        }

        // Keyboard navigation
        document.addEventListener('keydown', (e) => {
            if (e.key === 'ArrowRight' || e.key === ' ' || e.key === 'PageDown') {
                nextSlide();
            } else if (e.key === 'ArrowLeft' || e.key === 'PageUp') {
                prevSlide();
            }
        });

        // Initialize total slides display
        document.getElementById('total-slides').innerText = totalSlides;

        // Double click to toggle fullscreen (optional)
        document.addEventListener('dblclick', () => {
            if (!document.fullscreenElement) {
                document.documentElement.requestFullscreen();
            } else {
                if (document.exitFullscreen) {
                    document.exitFullscreen();
                }
            }
        });

    </script>
</body>
</html>
