www.akcaprox.com
<html lang="tr">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, user-scalable=yes">
  <meta name="mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <title>Kariyer Gelişim Envanteri</title>
  <style>
        body {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        * {
            box-sizing: border-box;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 10px 20px;
            min-height: 100vh;
            position: relative;
        }

        .admin-gear {
            position: fixed;
            top: 10px;
            left: 10px;
            width: 20px;
            height: 20px;
            cursor: pointer;
            opacity: 0.1;
            transition: all 0.3s ease;
            z-index: 10000;
            background: transparent;
            border-radius: 50%;
            padding: 5px;
        }

        .admin-gear:hover {
            opacity: 0.6;
            background: rgba(255, 255, 255, 0.2);
            transform: rotate(90deg);
        }

        .admin-gear svg {
            width: 100%;
            height: 100%;
            fill: white;
        }

        .login-screen, .register-screen, .welcome-screen {
            background: white;
            border-radius: 20px;
            padding: 15px 30px;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
        }

        .admin-panel {
            background: white;
            border-radius: 20px;
            padding: 20px 30px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            margin-bottom: 20px;
            max-width: 100%;
            width: 100%;
            margin-left: 0;
            margin-right: 0;
        }

        .admin-panel h1 {
            font-size: 1.75rem;
            margin-bottom: 5px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-align: center;
        }

        .login-screen h1, .register-screen h1, .welcome-screen h1 {
            font-size: 1.75rem;
            margin-bottom: 5px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .form-group {
            margin-bottom: 16px;
            text-align: left;
        }

        .form-group label {
            display: block;
            margin-bottom: 6px;
            font-weight: 600;
            color: #333;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 10px;
            border: 2px solid #e9ecef;
            border-radius: 8px;
            font-size: 0.95rem;
            transition: border-color 0.3s ease;
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
        }

        .form-group input:focus, .form-group select:focus {
            outline: none;
            border-color: #667eea;
        }

        .btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 12px 32px;
            font-size: 1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
            margin: 8px;
            -webkit-tap-highlight-color: transparent;
            touch-action: manipulation;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 30px rgba(102, 126, 234, 0.4);
        }

        .btn:active {
            transform: translateY(0);
        }

        .btn:disabled {
            background: #ccc;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .btn-secondary {
            background: #6c757d;
            box-shadow: 0 10px 20px rgba(108, 117, 125, 0.3);
        }

        .btn-secondary:hover {
            background: #5a6268;
            box-shadow: 0 15px 30px rgba(108, 117, 125, 0.4);
        }

        .password-info {
            background: #e3f2fd;
            border: 1px solid #2196f3;
            border-radius: 8px;
            padding: 15px;
            margin: 20px 0;
            text-align: center;
        }

        .linkedin-link {
            color: #0077b5;
            text-decoration: none;
            font-weight: bold;
        }

        .linkedin-link:hover {
            text-decoration: underline;
        }

        .quiz-container {
            display: none;
            background: white;
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }

        .progress-bar {
            width: 100%;
            height: 6px;
            background: #e0e0e0;
            border-radius: 4px;
            margin-bottom: 20px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 4px;
            transition: width 0.3s ease;
            width: 0%;
        }

        .question-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding-bottom: 12px;
            border-bottom: 2px solid #f0f0f0;
        }

        .question-counter {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 6px 14px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 0.85rem;
        }

        .category-badge {
            background: #f8f9fa;
            color: #667eea;
            padding: 6px 14px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 0.85rem;
            border: 2px solid #667eea;
        }

        .question-text {
            font-size: 1.15rem;
            font-weight: 600;
            margin-bottom: 20px;
            line-height: 1.5;
            color: #2c3e50;
        }

        .options-container {
            display: grid;
            gap: 12px;
            margin-bottom: 25px;
        }

        .option {
            background: #f8f9fa;
            border: 2px solid #e9ecef;
            border-radius: 12px;
            padding: 16px;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            -webkit-tap-highlight-color: transparent;
            touch-action: manipulation;
            user-select: none;
            -webkit-user-select: none;
        }

        .option:hover {
            border-color: #667eea;
            background: #f0f4ff;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.1);
        }

        .option:active {
            transform: translateY(0);
        }

        .option.selected {
            border-color: #667eea;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }

        .option-label {
            font-weight: bold;
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        .option-text {
            line-height: 1.5;
            font-size: 1rem;
        }

        .navigation-buttons {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-btn {
            padding: 12px 30px;
            border: none;
            border-radius: 25px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .prev-btn {
            background: #6c757d;
            color: white;
        }

        .prev-btn:hover {
            background: #5a6268;
            transform: translateY(-2px);
        }

        .next-btn {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
        }

        .next-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 20px rgba(102, 126, 234, 0.3);
        }

        .next-btn:disabled {
            background: #ccc;
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        .results-container, .report-container {
            display: none;
            background: white;
            border-radius: 20px;
            padding: 20px 35px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .results-header {
            text-align: center;
            margin-bottom: 20px;
        }

        .results-title {
            font-size: 1.75rem;
            margin-bottom: 8px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .overall-score {
            font-size: 2.5rem;
            font-weight: bold;
            color: #667eea;
            margin: 12px 0;
        }

        .score-interpretation {
            font-size: 1.1rem;
            color: #666;
            margin-bottom: 25px;
        }

        .category-results {
            display: grid;
            gap: 12px;
            margin-bottom: 20px;
        }

        .category-result {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 12px 16px;
            border-left: 4px solid #667eea;
        }

        .category-name {
            font-weight: bold;
            font-size: 1.05rem;
            margin-bottom: 8px;
            color: #2c3e50;
        }

        .category-score {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .score-bar {
            flex: 1;
            height: 10px;
            background: #e0e0e0;
            border-radius: 5px;
            margin: 0 15px;
            overflow: hidden;
        }

        .score-fill {
            height: 100%;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 5px;
            transition: width 0.5s ease;
        }

        .score-value {
            font-weight: bold;
            color: #667eea;
            min-width: 60px;
            text-align: right;
        }

        .admin-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            overflow-x: auto;
            display: block;
        }

        .admin-table th, .admin-table td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
            font-size: 0.9rem;
        }

        .admin-table th {
            background: #f8f9fa;
            font-weight: bold;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        .admin-table tr:nth-child(even) {
            background: #f9f9f9;
        }

        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid #f3f3f3;
            border-top: 3px solid #667eea;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateX(-50%) translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(-50%) translateY(0);
            }
        }

        @keyframes slideUp {
            from {
                opacity: 1;
                transform: translateX(-50%) translateY(0);
            }
            to {
                opacity: 0;
                transform: translateX(-50%) translateY(-20px);
            }
        }

        .hidden {
            display: none !important;
        }

        .chart-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            margin: 30px 0;
        }

        .chart-box {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 20px;
            text-align: center;
            border: 2px solid #e9ecef;
        }

        .chart-title {
            font-size: 1.1rem;
            font-weight: bold;
            margin-bottom: 15px;
            color: #2c3e50;
        }

        .chart-canvas {
            width: 100%;
            height: 280px;
            background: white;
            border-radius: 10px;
            border: 1px solid #dee2e6;
        }

        .analysis-section {
            margin: 20px 0;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 15px;
            border-left: 5px solid #667eea;
        }

        .analysis-title {
            font-size: 1.6rem;
            font-weight: bold;
            color: #667eea;
            margin-bottom: 15px;
            text-align: center;
        }

        .disclaimer {
            background: #fff3cd;
            border: 2px solid #ffc107;
            border-radius: 10px;
            padding: 15px;
            margin: 20px 0;
            color: #856404;
        }

        .disclaimer-title {
            font-weight: bold;
            font-size: 1.05rem;
            margin-bottom: 8px;
            color: #dc3545;
        }

        .category-analysis {
            margin: 25px 0;
            padding: 20px;
            background: white;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }

        .category-analysis h4 {
            color: #667eea;
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .category-analysis p {
            line-height: 1.6;
            color: #495057;
            margin-bottom: 10px;
        }

        .ai-analysis-box {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            border-left: 5px solid #667eea;
            padding: 25px;
            margin: 20px 0;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .ai-analysis-title {
            color: #667eea;
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .ai-badge {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        .analysis-subsection {
            margin: 15px 0;
            padding: 15px;
            background: white;
            border-radius: 8px;
        }

        .analysis-subsection h5 {
            color: #764ba2;
            font-size: 1.1rem;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .analysis-subsection ul {
            list-style: none;
            padding-left: 0;
        }

        .analysis-subsection li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
        }

        .analysis-subsection li:before {
            content: "▸";
            position: absolute;
            left: 5px;
            color: #667eea;
            font-weight: bold;
        }

        .score-badge {
            display: inline-block;
            padding: 5px 12px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 0.9rem;
            margin-left: 10px;
        }

        .score-excellent { background: #d4edda; color: #155724; }
        .score-good { background: #d1ecf1; color: #0c5460; }
        .score-average { background: #fff3cd; color: #856404; }
        .score-needs-improvement { background: #f8d7da; color: #721c24; }

        /* PDF Export Styles */
        .pdf-container {
            background: white;
            padding: 40px;
            max-width: 800px;
            margin: 0 auto;
        }

        .pdf-header {
            text-align: center;
            margin-bottom: 30px;
            border-bottom: 3px solid #667eea;
            padding-bottom: 20px;
        }

        .pdf-header h1 {
            color: #667eea;
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .pdf-info {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 30px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
        }

        .pdf-info-item {
            padding: 10px;
        }

        .pdf-info-label {
            font-weight: bold;
            color: #667eea;
            font-size: 0.9rem;
        }

        .pdf-info-value {
            font-size: 1rem;
            margin-top: 5px;
        }

        .pdf-section {
            margin-bottom: 30px;
            page-break-inside: avoid;
        }

        .pdf-section-title {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 12px 20px;
            border-radius: 8px;
            margin-bottom: 15px;
            font-size: 1.3rem;
            font-weight: bold;
        }

        .pdf-chart-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin: 20px 0;
        }

        .pdf-chart-item {
            text-align: center;
            page-break-inside: avoid;
        }

        .pdf-chart-item h4 {
            margin-bottom: 10px;
            color: #667eea;
        }

        @media print {
            body {
                background: white;
            }
            
            .pdf-container {
                padding: 20px;
            }
            
            .pdf-section {
                page-break-inside: avoid;
            }
        }

        @media (max-width: 768px) {
            body {
                font-size: 14px;
                padding: 0;
            }

            .container {
                padding: 5px;
                margin: 0;
            }
            
            .login-screen, .register-screen, .welcome-screen, .quiz-container, .results-container, .report-container, .admin-panel {
                padding: 15px;
                border-radius: 12px;
                margin: 5px;
                width: calc(100% - 10px);
            }

            .chart-container {
                grid-template-columns: 1fr;
                gap: 15px;
                padding: 10px 0;
            }
            
            .login-screen h1, .register-screen h1, .welcome-screen h1 {
                font-size: 1.8rem;
            }

            .admin-panel h1 {
                font-size: 1.6rem;
            }
            
            .question-text {
                font-size: 1rem;
                line-height: 1.4;
            }
            
            .option {
                padding: 12px;
            }

            .option-label {
                font-size: 1rem;
            }

            .option-text {
                font-size: 0.9rem;
            }
            
            .navigation-buttons {
                flex-direction: column;
                gap: 10px;
            }
            
            .nav-btn, .btn {
                width: 100%;
                padding: 12px 20px;
                font-size: 1rem;
            }

            .prev-btn, .next-btn {
                padding: 10px 20px;
            }

            .admin-table {
                font-size: 0.7rem;
                overflow-x: auto;
                display: block;
                width: 100%;
                -webkit-overflow-scrolling: touch;
            }

            .admin-table th, .admin-table td {
                padding: 8px 4px;
                white-space: nowrap;
                font-size: 11px;
                min-width: 80px;
            }
            
            .admin-table thead {
                position: sticky;
                top: 0;
                background: white;
                z-index: 10;
            }

            .results-title {
                font-size: 1.8rem;
            }

            .overall-score {
                font-size: 2.5rem;
            }

            .score-interpretation {
                font-size: 1rem;
            }

            .category-name {
                font-size: 1rem;
            }

            .chart-title {
                font-size: 1rem;
            }

            .analysis-title {
                font-size: 1.5rem;
            }

            .category-analysis h4 {
                font-size: 1.1rem;
            }

            .category-analysis p {
                font-size: 0.9rem;
            }

            .form-group input, .form-group select {
                padding: 10px;
                font-size: 0.95rem;
            }

            .question-header {
                flex-direction: column;
                gap: 10px;
                align-items: flex-start;
            }

            .question-counter, .category-badge {
                font-size: 0.85rem;
                padding: 6px 12px;
            }

            .disclaimer {
                padding: 15px;
            }

            .disclaimer-title {
                font-size: 1rem;
            }

            .chart-canvas {
                height: 250px;
                max-width: 100%;
            }

            .admin-gear {
                top: 5px;
                left: 5px;
                width: 18px;
                height: 18px;
            }
            
            .pdf-info {
                grid-template-columns: 1fr !important;
                gap: 10px;
            }
            
            .pdf-chart-grid {
                grid-template-columns: 1fr !important;
            }
        }

        /* Çok küçük ekranlar için ekstra optimizasyon */
        @media (max-width: 480px) {
            .container {
                padding: 3px;
                max-width: 100%;
            }

            .login-screen, .register-screen, .welcome-screen, .quiz-container, .results-container, .report-container, .admin-panel {
                padding: 12px;
                border-radius: 10px;
                margin: 3px;
                width: calc(100% - 6px);
            }

            .login-screen h1, .register-screen h1, .welcome-screen h1 {
                font-size: 1.5rem;
                margin-bottom: 10px;
            }

            .question-text {
                font-size: 0.95rem;
            }

            .option {
                padding: 10px;
            }

            .option-label {
                font-size: 0.9rem;
            }

            .option-text {
                font-size: 0.85rem;
            }

            .btn {
                padding: 10px 15px;
                font-size: 0.95rem;
                margin: 5px 0;
            }

            .overall-score {
                font-size: 2rem;
            }

            .results-title {
                font-size: 1.5rem;
            }

            .analysis-title {
                font-size: 1.3rem;
            }

            .category-analysis {
                padding: 15px;
            }

            .chart-canvas {
                height: 200px;
                max-width: 100%;
            }

            .form-group {
                margin-bottom: 12px;
            }
            
            .form-group input,
            .form-group select {
                font-size: 16px !important;
                min-height: 44px;
            }
            
            .pdf-info {
                grid-template-columns: 1fr;
                gap: 10px;
            }
            
            .pdf-chart-grid {
                grid-template-columns: 1fr;
            }
            
            #disclaimerModal > div {
                margin: 10px;
                padding: 20px;
                max-width: calc(100% - 20px);
            }
            
            #disclaimerModal h2 {
                font-size: 1.2rem;
            }
            
            #disclaimerModal h3 {
                font-size: 1rem;
            }
            
            #disclaimerModal p {
                font-size: 0.9rem;
            }
        }

        /* Landscape mod için tablet optimizasyonu */
        @media (min-width: 769px) and (max-width: 1024px) {
            .container {
                max-width: 95%;
                padding: 15px;
            }

            .chart-container {
                grid-template-columns: 1fr 1fr;
            }
        }

        /* Touch-friendly özellikler */
        @media (hover: none) and (pointer: coarse) {
            .option {
                min-height: 60px;
                touch-action: manipulation;
                -webkit-tap-highlight-color: transparent;
            }

            .btn, .nav-btn {
                min-height: 48px;
                touch-action: manipulation;
                -webkit-tap-highlight-color: transparent;
                font-size: 16px;
            }

            .form-group input, .form-group select {
                min-height: 48px;
                font-size: 16px;
            }

            .admin-gear {
                width: 35px;
                height: 35px;
                padding: 10px;
                top: 5px;
                left: 5px;
            }
            
            a, button, input, select, textarea {
                -webkit-tap-highlight-color: transparent;
            }
        }
    </style>
  
  <style>
    /* Google Auth Button */
    .google-auth-btn {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        color: white;
        border: 2px solid rgba(255, 255, 255, 0.3);
        padding: 12px 24px;
        font-size: 16px;
        font-weight: 500;
        border-radius: 8px;
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 12px;
        transition: all 0.3s ease;
        margin: 15px 0;
        width: 100%;
        box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
    }

    .google-auth-btn:hover {
        background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
        border-color: rgba(255, 255, 255, 0.5);
        box-shadow: 0 12px 30px rgba(102, 126, 234, 0.5);
        transform: translateY(-2px);
    }

    .google-auth-btn svg {
        width: 24px;
        height: 24px;
    }

    /* Firebase Auth Status Box */
    .firebase-auth-status {
        position: fixed;
        top: 20px;
        right: 20px;
        background: linear-gradient(135deg, #4caf50 0%, #45a049 100%);
        padding: 20px 25px;
        border-radius: 15px;
        box-shadow: 0 8px 32px rgba(76, 175, 80, 0.4);
        z-index: 9999;
        animation: slideInRight 0.5s ease, pulse 2s infinite;
        min-width: 300px;
        border: 2px solid rgba(255, 255, 255, 0.3);
    }

    .firebase-auth-status.hidden {
        display: none;
    }

    .firebase-auth-status h3 {
        color: white;
        margin: 0 0 10px 0;
        font-size: 18px;
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .firebase-auth-status p {
        color: rgba(255, 255, 255, 0.95);
        margin: 5px 0;
        font-size: 14px;
    }

    .firebase-auth-status .email {
        background: rgba(255, 255, 255, 0.2);
        padding: 8px 12px;
        border-radius: 8px;
        font-weight: bold;
        color: #fff;
        margin-top: 8px;
        word-break: break-all;
        border: 1px solid rgba(255, 255, 255, 0.3);
    }

    .status-icon {
        display: inline-block;
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background: #4caf50;
        animation: blink 1.5s infinite;
        box-shadow: 0 0 10px #4caf50;
    }

    @keyframes slideInRight {
        from {
            transform: translateX(400px);
            opacity: 0;
        }
        to {
            transform: translateX(0);
            opacity: 1;
        }
    }

    @keyframes pulse {
        0%, 100% {
            box-shadow: 0 8px 32px rgba(76, 175, 80, 0.4);
        }
        50% {
            box-shadow: 0 8px 32px rgba(69, 160, 73, 0.6), 
                        0 0 40px rgba(102, 126, 234, 0.3);
        }
    }

    @keyframes blink {
        0%, 100% {
            opacity: 1;
            box-shadow: 0 0 10px #4caf50;
        }
        50% {
            opacity: 0.3;
            box-shadow: 0 0 5px #4caf50;
        }
    }

    @keyframes rainbow {
        0% { border-color: #ff0000; }
        14% { border-color: #ff7f00; }
        28% { border-color: #ffff00; }
        42% { border-color: #00ff00; }
        57% { border-color: #0000ff; }
        71% { border-color: #4b0082; }
        85% { border-color: #9400d3; }
        100% { border-color: #ff0000; }
    }

    .firebase-auth-status.rainbow-border {
        animation: slideInRight 0.5s ease, pulse 2s infinite, rainbow 3s linear infinite;
        border-width: 3px;
    }

    .close-status-btn {
        position: absolute;
        top: 10px;
        right: 10px;
        background: rgba(255, 255, 255, 0.2);
        border: none;
        color: white;
        width: 25px;
        height: 25px;
        border-radius: 50%;
        cursor: pointer;
        font-size: 16px;
        line-height: 1;
        transition: all 0.3s;
    }

    .close-status-btn:hover {
        background: rgba(255, 255, 255, 0.4);
        transform: rotate(90deg);
    }

    /* Mobile responsive */
    @media (max-width: 768px) {
        .firebase-auth-status {
            top: 5px;
            right: 5px;
            left: 5px;
            min-width: auto;
            max-width: calc(100% - 10px);
            padding: 12px;
            font-size: 13px;
        }
        
        .firebase-auth-status h3 {
            font-size: 14px;
        }
        
        .firebase-auth-status .email {
            font-size: 12px;
            word-break: break-all;
            padding: 6px 8px;
        }
        
        .google-auth-btn {
            padding: 12px 16px;
            font-size: 14px;
        }
        
        .google-auth-btn svg {
            width: 20px;
            height: 20px;
        }
    }
  </style>
  
  <style>@view-transition { navigation: auto; }</style>
  
  <!-- Firebase SDK -->
  <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-auth-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-database-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-analytics-compat.js"></script>
  
  <!-- PDF Libraries -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/polyfills.umd.min.js"></script>
 </head>
 <body>
  <div class="container"><!-- Admin Gear Button -->
   <div class="admin-gear" onclick="showAdminLogin()">
    <svg viewbox="0 0 24 24"><path d="M12,15.5A3.5,3.5 0 0,1 8.5,12A3.5,3.5 0 0,1 12,8.5A3.5,3.5 0 0,1 15.5,12A3.5,3.5 0 0,1 12,15.5M19.43,12.97C19.47,12.65 19.5,12.33 19.5,12C19.5,11.67 19.47,11.34 19.43,11L21.54,9.37C21.73,9.22 21.78,8.95 21.66,8.73L19.66,5.27C19.54,5.05 19.27,4.96 19.05,5.05L16.56,6.05C16.04,5.66 15.5,5.32 14.87,5.07L14.5,2.42C14.46,2.18 14.25,2 14,2H10C9.75,2 9.54,2.18 9.5,2.42L9.13,5.07C8.5,5.32 7.96,5.66 7.44,6.05L4.95,5.05C4.73,4.96 4.46,5.05 4.34,5.27L2.34,8.73C2.22,8.95 2.27,9.22 2.46,9.37L4.57,11C4.53,11.34 4.5,11.67 4.5,12C4.5,12.33 4.53,12.65 4.57,12.97L2.46,14.63C2.27,14.78 2.22,15.05 2.34,15.27L4.34,18.73C4.46,18.95 4.73,19.03 4.95,18.95L7.44,17.94C7.96,18.34 8.5,18.68 9.13,18.93L9.5,21.58C9.54,21.82 9.75,22 10,22H14C14.25,22 14.46,21.82 14.5,21.58L14.87,18.93C15.5,18.68 16.04,18.34 16.56,17.94L19.05,18.95C19.27,19.03 19.54,18.95 19.66,18.73L21.66,15.27C21.78,15.05 21.73,14.78 21.54,14.63L19.43,12.97Z" />
    </svg>
   </div><!-- Login Screen -->
   <div class="login-screen" id="loginScreen">
    <h1 id="loginTitle">Kariyer Gelişim Performansı ve İlerleme Paneli</h1>

    <div style="background: #fff3cd; border: 1px solid #ffc107; border-radius: 8px; padding: 12px; margin-bottom: 15px; font-size: 0.9rem; color: #856404;">
        <strong>🔐 Bilgilendirme:</strong> Panele erişim için Google ile giriş yapmanız gerekmektedir. Güvenlik nedeniyle zorunludur.
    </div>
    
    <!-- Sorumluluk Reddi Butonu -->
    <div style="text-align: center; margin-bottom: 20px;">
        <button type="button" id="disclaimerBtn" onclick="showDisclaimerModal()" style="
            background: linear-gradient(135deg, #f5576c 0%, #f093fb 100%);
            color: white;
            border: none;
            padding: 10px 24px;
            font-size: 0.9rem;
            border-radius: 25px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(245, 87, 108, 0.3);
            transition: all 0.3s ease;
        ">
            ⚖️ Sorumluluk Reddi ve Gizlilik Beyanı
        </button>
    </div>

    <!-- Google Auth Button / Status -->
    <div id="googleAuthContainer">
        <button type="button" class="google-auth-btn" onclick="checkDisclaimerAndLogin()" id="googleLoginBtn">
            <svg viewBox="0 0 24 24">
                <path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/>
                <path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/>
                <path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"/>
                <path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/>
            </svg>
            Google ile Giriş Yap
        </button>
        
        <!-- Firebase Auth Status (butonun yerine gelecek) -->
        <div id="firebaseAuthStatus" class="firebase-auth-status hidden">
            <button class="close-status-btn" onclick="closeAuthStatus()">×</button>
            <h3>
                <span class="status-icon"></span>
                ✅ Google ile Giriş Yapıldı!
            </h3>
            <p id="authMethodText">Bağlantı kuruldu</p>
            <div class="email" id="authEmailDisplay"></div>
        </div>
    </div>

    <form id="loginForm" onsubmit="handleLogin(event)">
     <div class="form-group"><label for="loginNickname">Rumuz:</label> <input type="text" id="loginNickname" required disabled>
     </div>
     <div class="form-group"><label for="loginPassword">Şifre:</label> <input type="password" id="loginPassword" required disabled>
     </div>
     <button type="submit" class="btn" id="loginBtn" disabled style="opacity: 0.5; cursor: not-allowed;"> 
         <span class="btn-text">Giriş Yap</span> <span class="loading hidden"></span> 
     </button> 
     <button type="button" class="btn btn-secondary" id="registerBtn" onclick="showRegister()" disabled style="opacity: 0.5; cursor: not-allowed;">Üye Ol</button>
     <p style="text-align: center; color: #999; font-size: 0.85rem; margin-top: 15px;">
         ℹ️ Önce Google ile giriş yapmanız gerekiyor
     </p>
    </form>
   </div><!-- Register Screen -->
   <div class="register-screen hidden" id="registerScreen">
    <h1>Üye Kayıt</h1>
    
    <div id="googleAuthInfo" class="firebase-auth-status" style="position: relative; margin-bottom: 20px; display: none;">
        <h3 style="color: white; margin: 0 0 10px 0; font-size: 16px;">
            <span class="status-icon"></span>
            Google ile Bağlantı Kuruldu
        </h3>
        <div class="email" id="registerGoogleEmail" style="background: rgba(255,255,255,0.2); padding: 8px; border-radius: 6px; font-size: 14px;"></div>
        <p style="color: rgba(255,255,255,0.9); margin: 10px 0 0 0; font-size: 13px;">
            ℹ️ Kayıt sonrası rumuz ve şifre ile giriş yapmanız gerekecek.
        </p>
    </div>
    
    <form id="registerForm" onsubmit="handleRegister(event)">
     <div class="form-group"><label for="nickname">Rumuz:</label> <input type="text" id="nickname" required>
      <div style="background: #e8f4fd; border: 1px solid #bee5eb; border-radius: 6px; padding: 10px; margin-top: 8px; font-size: 0.9rem; color: #0c5460;"><strong>🔒 Gizlilik Notu:</strong> Lütfen kişisel bilgilerde isim-soyisim kullanmayınız. Rumuz sistemi kişiselliğinizi korumak için yapılmıştır.
      </div>
     </div>
     <div class="form-group"><label for="phone">Telefon Numarası:</label> <input type="tel" id="phone" required>
     </div>
     <div class="form-group"><label for="education">Mezuniyet Durumu:</label> <select id="education" required> <option value="">Seçiniz</option> <option value="Lise">Lise</option> <option value="Ön Lisans">Ön Lisans</option> <option value="Lisans">Lisans</option> <option value="Yüksek Lisans">Yüksek Lisans</option> <option value="Doktora">Doktora</option> </select>
     </div>
     <div class="form-group"><label for="department">Bölüm:</label> <input type="text" id="department" required>
     </div>
     <div class="form-group"><label for="position">Şu Anki İş Pozisyonu:</label> <input type="text" id="position" required>
     </div>
     <div class="password-info">
      <p><strong>Önemli:</strong> Kayıt işleminiz tamamlandıktan sonra sistem otomatik olarak 6 basamaklı bir şifre oluşturacaktır.</p>
      <p>Bu şifreyi almak için aşağıdaki bağlantıdan yöneticiye ulaşın:</p><a href="https://www.linkedin.com/in/bar%C4%B1%C5%9F-ak%C3%A7a-46997593/" target="_blank" class="linkedin-link">Şifre almak için tıklayın</a>
     </div><button type="submit" class="btn" id="submitRegisterBtn"> <span class="btn-text">Kayıt Ol</span> <span class="loading hidden"></span> </button> <button type="button" class="btn btn-secondary" onclick="showLogin()">Giriş Ekranına Dön</button>
    </form>
   </div><!-- Admin Login Screen -->
   <div class="admin-panel hidden" id="adminLoginScreen">
    <h1>🔐 Admin Girişi</h1>
    
    <div style="background: linear-gradient(135deg, #ff6b6b 0%, #ee5a6f 100%); border: 2px solid #ff4757; border-radius: 10px; padding: 15px; margin-bottom: 20px; color: white; box-shadow: 0 4px 15px rgba(255, 75, 87, 0.3);">
        <h3 style="margin: 0 0 10px 0; font-size: 16px;">⚠️ SÜPER ADMIN GÜVENLİK UYARISI</h3>
        <p style="margin: 5px 0; font-size: 14px; line-height: 1.5;">
            Admin paneline <strong>sadece "analizprox@gmail.com" hesabı</strong> erişebilir.
        </p>
        <p style="margin: 5px 0; font-size: 13px; opacity: 0.9;">
            🔒 Google ile kimlik doğrulaması yapmanız zorunludur.
        </p>
        <p style="margin: 5px 0; font-size: 13px; opacity: 0.9;">
            ⚡ Yetkisiz giriş denemeleri otomatik olarak kaydedilir ve engellenir.
        </p>
    </div>

    <div id="adminGoogleAuthStatus" style="display: none; background: linear-gradient(135deg, #4caf50 0%, #45a049 100%); border-radius: 10px; padding: 15px; margin-bottom: 20px; color: white;">
        <h3 style="margin: 0 0 10px 0; font-size: 16px;">
            <span class="status-icon" style="background: white;"></span>
            ✅ Google Kimlik Doğrulaması Başarılı
        </h3>
        <div style="background: rgba(255,255,255,0.2); padding: 10px; border-radius: 6px; margin-top: 10px;">
            <strong>Süper Admin:</strong> <span id="adminGoogleEmail"></span>
        </div>
        <p style="margin: 10px 0 0 0; font-size: 13px; opacity: 0.9;">
            Şimdi admin şifrenizi girerek panele erişebilirsiniz.
        </p>
    </div>

    <button type="button" class="google-auth-btn" onclick="adminGoogleLogin()" id="adminGoogleBtn">
        <svg viewBox="0 0 24 24">
            <path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/>
            <path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/>
            <path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"/>
            <path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"/>
        </svg>
        🔐 Google ile Admin Girişi Yap
    </button>

    <form id="adminLoginForm" onsubmit="handleAdminLogin(event)" style="display: none;">
     <div class="form-group"><label for="adminPassword">Admin Şifresi:</label> <input type="password" id="adminPassword" required>
     </div><button type="submit" class="btn">Admin Paneline Gir</button> <button type="button" class="btn btn-secondary" onclick="hideAdminLogin()">İptal</button>
    </form>
   </div><!-- Admin Panel -->
   <div class="admin-panel hidden" id="adminPanel">
    <h1>Kariyer Gelişim Performansı ve İlerleme Paneli</h1><button class="btn btn-secondary" onclick="hideAdmin()" style="float: right;">Kapat</button>
    <div id="adminContent">
     <div class="loading"></div>
     <p>Veriler yükleniyor...</p>
    </div>
   </div><!-- Welcome Screen -->
   <div class="welcome-screen hidden" id="welcomeScreen">
    <h1 id="mainTitle">Kariyer Gelişim Envanteri</h1>
    <p id="subtitle">Profesyonel Yetkinlik Değerlendirme Sistemi</p>
    <p>Bu envanter, kariyer gelişiminizde kritik olan 10 temel yetkinlik alanını değerlendirmenizi sağlar. Her alan için 10 soru olmak üzere toplam 100 soruyu yanıtlayarak, güçlü yönlerinizi ve gelişim alanlarınızı keşfedeceksiniz.</p>
    <button class="btn" onclick="startQuiz()">Envanteri Başlat</button> 
    <button class="btn" onclick="showMyReports()" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">📊 Geçmiş Raporlarım</button>
    <button class="btn btn-secondary" onclick="logout()">Çıkış Yap</button>
   </div>
   
   <!-- Sorumluluk Reddi Modal -->
   <div id="disclaimerModal" style="display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); z-index: 99999; overflow-y: auto;">
    <div style="max-width: 800px; margin: 30px auto; background: white; border-radius: 20px; padding: 30px; position: relative; box-shadow: 0 10px 50px rgba(0,0,0,0.3);">
        <button class="disclaimer-close-btn" onclick="closeDisclaimerModal()" style="position: absolute; top: 15px; right: 15px; background: #f44336; color: white; border: none; width: 40px; height: 40px; border-radius: 50%; font-size: 24px; cursor: pointer; line-height: 1; display: flex; align-items: center; justify-content: center;">×</button>
        
        <h2 style="color: #667eea; margin-bottom: 20px; text-align: center;">⚖️ Sorumluluk Reddi ve Gizlilik Beyanı</h2>
        
        <div style="max-height: 60vh; overflow-y: auto; padding: 20px; background: #f9f9f9; border-radius: 10px; margin-bottom: 20px;">
            <h3 style="color: #333; margin-top: 0;">1. Genel Bilgilendirme</h3>
            <p style="line-height: 1.6;">Bu Kariyer Gelişim Envanteri, kişisel değerlendirme ve gelişim amaçlı bir araçtır. Test sonuçları genel bir değerlendirme niteliğindedir ve profesyonel kariyer danışmanlığının yerini tutmaz.</p>
            
            <h3 style="color: #333;">2. Profesyonel Danışmanlık Gereksinimi</h3>
            <p style="line-height: 1.6;"><strong>ÖNEMLİ:</strong> Bu analizin yorumlanması için mutlaka profesyonel bir destek ve danışmanlık alınız. Bireysel çıkarımlar sizi hatalı değerlendirmelere sevk edebilir.</p>
            
            <h3 style="color: #333;">3. Gizlilik ve Veri Güvenliği</h3>
            <p style="line-height: 1.6;">Verileriniz Firebase Realtime Database'de güvenli bir şekilde saklanmaktadır. Kişisel bilgileriniz hiçbir şekilde üçüncü şahıslarla paylaşılmayacaktır. Rumuz sistemi, gizliliğinizi korumak için tasarlanmıştır - lütfen gerçek isim-soyisim kullanmayınız.</p>
            
            <h3 style="color: #333;">4. Google Authentication</h3>
            <p style="line-height: 1.6;">Güvenlik nedeniyle sisteme giriş için Google kimlik doğrulaması zorunludur. Google hesabınız sadece kimlik doğrulama için kullanılır ve email adresiniz kayıt işlemi sırasında kaydedilir.</p>
            
            <h3 style="color: #333;">5. Test Sonuçları</h3>
            <p style="line-height: 1.6;">Test sonuçları, belirli bir zamandaki durumunuzu yansıtır ve zaman içinde değişebilir. Sonuçlar, kariyer kararlarınızda tek başına belirleyici olmamalıdır.</p>
            
            <h3 style="color: #333;">6. Sorumluluk Reddi</h3>
            <p style="line-height: 1.6;">Bu envanter sonuçlarına dayanarak alınan kararlardan ve bunların sonuçlarından platform geliştiricisi sorumlu değildir. Tüm kararlarınızı profesyonel danışmanlık eşliğinde almanızı tavsiye ederiz.</p>
            
            <h3 style="color: #333;">7. Veri Saklama</h3>
            <p style="line-height: 1.6;">Test geçmişiniz ve sonuçlarınız Firebase'de güvenli bir şekilde saklanır. Hesabınızı silmek isterseniz, sistem yöneticisi ile iletişime geçebilirsiniz.</p>
        </div>
        
        <div id="disclaimerActions" style="display: flex; flex-direction: column; gap: 15px; align-items: center;">
            <label style="display: flex; align-items: center; gap: 10px; font-size: 16px; cursor: pointer;">
                <input type="checkbox" id="disclaimerAccept" style="width: 20px; height: 20px; cursor: pointer;">
                <span>Yukarıdaki metni okudum, anladım ve kabul ediyorum.</span>
            </label>
            
            <button id="acceptDisclaimerBtn" onclick="acceptDisclaimer()" disabled style="
                background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
                color: white;
                border: none;
                padding: 15px 40px;
                font-size: 16px;
                border-radius: 30px;
                cursor: not-allowed;
                opacity: 0.5;
                transition: all 0.3s;
            ">
                ✅ Kabul Ediyorum ve Devam Et
            </button>
        </div>
    </div>
   </div>

   <!-- My Reports Screen -->
   <div class="welcome-screen hidden" id="myReportsScreen">
    <h1>📊 Geçmiş Raporlarım</h1>
    <p style="text-align: center; color: #666; margin-bottom: 30px;">Test geçmişinizi görüntüleyin ve raporlarınızı karşılaştırın</p>
    
    <div id="reportsHistory" style="max-width: 1000px; margin: 0 auto;"></div>
    
    <div style="margin-top: 30px;">
        <button class="btn btn-secondary" onclick="backToWelcomeFromReports()">← Ana Menüye Dön</button>
    </div>
   </div>
   
   <!-- Quiz Container -->
   <div class="quiz-container" id="quizContainer">
    <div class="progress-bar">
     <div class="progress-fill" id="progressFill"></div>
    </div>
    <div class="question-header">
     <div class="question-counter" id="questionCounter">
      Soru 1 / 100
     </div>
     <div class="category-badge" id="categoryBadge">
      Kategori
     </div>
    </div>
    <div class="question-text" id="questionText"></div>
    <div class="options-container" id="optionsContainer"></div>
    <div class="navigation-buttons"><button class="nav-btn prev-btn" id="prevBtn" onclick="previousQuestion()">← Önceki</button> <button class="nav-btn next-btn" id="nextBtn" onclick="nextQuestion()" disabled>Sonraki →</button>
    </div>
   </div><!-- Results Container -->
   <div class="results-container" id="resultsContainer">
    <div class="results-header">
     <h2 class="results-title">Kariyer Gelişim Raporu</h2>
     <div class="overall-score" id="overallScore">
      0
     </div>
     <div class="score-interpretation" id="scoreInterpretation"></div>
    </div>
    <div class="category-results" id="categoryResults"></div>
    <div id="resultsActions">
        <button class="btn" onclick="showDetailedReport()">Detaylı Raporu Görüntüle</button> 
        <button class="btn" onclick="downloadPDFReport()">📄 PDF Rapor İndir</button> 
        <button class="btn btn-secondary" onclick="backToWelcome()">Ana Menüye Dön</button>
    </div>
   </div><!-- Report Container -->
   <div class="report-container" id="reportContainer">
    <div class="disclaimer">
     <div class="disclaimer-title">
      ⚠️ Önemli Uyarı
     </div>
     <p><strong>Bu analizin yorumlanması için mutlaka profesyonel bir destek ve danışmanlık alınız.</strong></p>
     <p>Bu rapor üzerinden yaptığınız bireysel çıkarımlar sizi hatalı değerlendirmelere sevk edebilir. Sonuçlar genel bir değerlendirme niteliğindedir ve profesyonel kariyer danışmanlığının yerini tutmaz.</p>
    </div>
    <div class="results-header">
     <h2 class="results-title">AKÇA PRO X ANALİZİ</h2>
     <div class="overall-score" id="reportOverallScore">
      0
     </div>
     <p style="text-align: center; color: #666; margin-bottom: 30px;">Detaylı Kariyer Yetkinlik Analizi</p>
    </div>
    <div class="chart-container">
     <div class="chart-box">
      <div class="chart-title">
       Radar Analizi
      </div>
      <canvas class="chart-canvas" id="radarChart"></canvas>
      <div id="radarChartLegend" style="margin-top: 15px;"></div>
     </div>
     <div class="chart-box">
      <div class="chart-title">
       Pasta Grafiği
      </div>
      <canvas class="chart-canvas" id="pieChart"></canvas>
      <div id="pieChartLegend" style="margin-top: 15px;"></div>
     </div>
     <div class="chart-box">
      <div class="chart-title">
       Çubuk Grafiği
      </div>
      <canvas class="chart-canvas" id="barChart"></canvas>
      <div id="barChartLegend" style="margin-top: 15px;"></div>
     </div>
     <div class="chart-box">
      <div class="chart-title">
       Nokta Grafiği
      </div>
      <canvas class="chart-canvas" id="scatterChart"></canvas>
      <div id="scatterChartLegend" style="margin-top: 15px;"></div>
     </div>
    </div>
    <div class="analysis-section">
     <div class="analysis-title">
      AKÇA PRO X ANALİZİ
     </div>
     <div id="categoryAnalyses"></div>
    </div><button class="btn" onclick="downloadDetailedPDFReport()">📄 Detaylı PDF Rapor İndir (Grafiklerle)</button> <button class="btn btn-secondary" onclick="backToResults()">Özet Sonuçlara Dön</button> <button class="btn btn-secondary" onclick="backToWelcome()">Ana Menüye Dön</button>
   </div>
  </div>
  <script>
        // Firebase Configuration
        const firebaseConfig = {
            apiKey: "AIzaSyBGYTJniNpr2ZGVTztQH00BPPXYNUI06uA",
            authDomain: "kariyer-gelisimi.firebaseapp.com",
            databaseURL: "https://kariyer-gelisimi-default-rtdb.europe-west1.firebasedatabase.app/",
            projectId: "kariyer-gelisimi",
            storageBucket: "kariyer-gelisimi.firebasestorage.app",
            messagingSenderId: "921683004788",
            appId: "1:921683004788:web:b8f9c712973cb863faf021",
            measurementId: "G-8F05T9J35B"
        };

        // Initialize Firebase
        firebase.initializeApp(firebaseConfig);
        const database = firebase.database();
        const auth = firebase.auth();
        const analytics = firebase.analytics();

        // Global değişkenler
        let currentUser = null;
        let allUsers = [];
        let currentQuestionIndex = 0;
        let answers = [];
        let currentCategoryIndex = 0;
        let currentQuestionInCategory = 0;
        let firebaseAuthUser = null; // Firebase Authentication kullanıcısı
        window.googleUser = null; // Google ile giriş yapan kullanıcı (global)
        const SUPER_ADMIN_EMAIL = "analizprox@gmail.com"; // Süper admin email
        let disclaimerAccepted = false; // Sorumluluk reddi onayı
        let currentUserEmail = null; // Mevcut kullanıcının email'i

        // Kullanıcıya özel disclaimer kontrolü
        function checkUserDisclaimer(email) {
            if (!email) return false;
            const disclaimerKey = 'disclaimer_' + email;
            return localStorage.getItem(disclaimerKey) === 'true';
        }

        function saveUserDisclaimer(email) {
            if (!email) return;
            const disclaimerKey = 'disclaimer_' + email;
            localStorage.setItem(disclaimerKey, 'true');
        }

        // Sorumluluk Reddi Modal Fonksiyonları
        function showDisclaimerModal(readOnlyMode = true) {
            document.getElementById('disclaimerModal').style.display = 'block';
            document.body.style.overflow = 'hidden'; // Scroll engelle
            
            // Checkbox'ı sıfırla
            const checkbox = document.getElementById('disclaimerAccept');
            if (checkbox) checkbox.checked = false;
            
            // Butonu devre dışı bırak
            const acceptBtn = document.getElementById('acceptDisclaimerBtn');
            const actionDiv = document.getElementById('disclaimerActions');
            const closeBtn = document.querySelector('.disclaimer-close-btn');
            
            if (readOnlyMode) {
                // Sadece okuma modu - checkbox ve onay butonu gizli
                if (actionDiv) actionDiv.style.display = 'none';
                if (closeBtn) closeBtn.style.display = 'block';
            } else {
                // Onay modu - checkbox ve onay butonu görünür
                if (actionDiv) actionDiv.style.display = 'flex';
                if (closeBtn) closeBtn.style.display = 'block';
                if (acceptBtn) {
                    acceptBtn.disabled = true;
                    acceptBtn.style.cursor = 'not-allowed';
                    acceptBtn.style.opacity = '0.5';
                }
            }
        }

        function closeDisclaimerModal() {
            document.getElementById('disclaimerModal').style.display = 'none';
            document.body.style.overflow = 'auto';
        }

        // Checkbox değişikliğini dinle
        document.addEventListener('DOMContentLoaded', function() {
            const checkbox = document.getElementById('disclaimerAccept');
            const acceptBtn = document.getElementById('acceptDisclaimerBtn');
            
            if (checkbox && acceptBtn) {
                checkbox.addEventListener('change', function() {
                    if (this.checked) {
                        acceptBtn.disabled = false;
                        acceptBtn.style.cursor = 'pointer';
                        acceptBtn.style.opacity = '1';
                    } else {
                        acceptBtn.disabled = true;
                        acceptBtn.style.cursor = 'not-allowed';
                        acceptBtn.style.opacity = '0.5';
                    }
                });
            }
        });

        function acceptDisclaimer() {
            if (currentUserEmail) {
                saveUserDisclaimer(currentUserEmail);
                disclaimerAccepted = true;
                closeDisclaimerModal();
                showMessage('✅ Sorumluluk reddi beyanı kabul edildi. Google girişi yapılıyor...', 'success');
                
                // Google giriş işlemini başlat
                setTimeout(() => {
                    signInWithGoogle();
                }, 500);
            } else {
                showMessage('❌ Bir hata oluştu. Lütfen tekrar deneyin.', 'error');
            }
        }

        // Google girişi öncesi disclaimer kontrolü
        async function checkDisclaimerAndLogin() {
            try {
                // Önce Google ile kimlik doğrula (popup aç)
                const provider = new firebase.auth.GoogleAuthProvider();
                provider.addScope('email');
                provider.addScope('profile');
                
                console.log('🔐 Google ile kimlik doğrulama yapılıyor...');
                
                const result = await auth.signInWithPopup(provider);
                const user = result.user;
                currentUserEmail = user.email;
                
                console.log('✅ Kimlik doğrulama başarılı:', currentUserEmail);
                
                // Bu kullanıcı daha önce disclaimer kabul etmiş mi?
                if (checkUserDisclaimer(currentUserEmail)) {
                    console.log('✅ Kullanıcı daha önce disclaimer kabul etmiş.');
                    disclaimerAccepted = true;
                    
                    // Direkt giriş yap
                    firebaseAuthUser = user;
                    window.googleUser = user;
                    
                    // Görsel bildirim göster
                    showAuthStatus(firebaseAuthUser.email, 'Google');
                    
                    // Form butonlarını aktif et
                    enableLoginButtons();
                    
                    // Kullanıcının sistemde kayıtlı olup olmadığını kontrol et
                    allUsers = await firebaseDB.getAll();
                    const existingUser = allUsers.find(u => u.google_email === firebaseAuthUser.email);
                    
                    if (existingUser) {
                        showMessage(`Merhaba ${firebaseAuthUser.displayName}! Sorumluluk reddi daha önce kabul edilmişti. Lütfen rumuz ve şifrenizle giriş yapın.`, 'success');
                    } else {
                        showMessage(`Merhaba ${firebaseAuthUser.displayName}! Sorumluluk reddi daha önce kabul edilmişti. Lütfen kayıt formunu doldurun.`, 'success');
                        showRegister();
                        
                        const googleAuthInfo = document.getElementById('googleAuthInfo');
                        const registerGoogleEmail = document.getElementById('registerGoogleEmail');
                        
                        if (googleAuthInfo && registerGoogleEmail) {
                            googleAuthInfo.style.display = 'block';
                            registerGoogleEmail.textContent = firebaseAuthUser.email;
                        }
                    }
                    
                    firebase.analytics().logEvent('login', {
                        method: 'Google'
                    });
                    
                } else {
                    console.log('⚠️ Kullanıcı disclaimer kabul etmemiş. Modal açılıyor...');
                    // Disclaimer kabul etmemiş, modal göster
                    showMessage(`Merhaba ${user.displayName}! Lütfen önce Sorumluluk Reddi ve Gizlilik Beyanını okuyup onaylayın.`, 'info');
                    
                    // Oturumu kapat (disclaimer kabul edilene kadar)
                    await auth.signOut();
                    
                    // Modal aç - onay modu
                    showDisclaimerModal(false);
                }
                
            } catch (error) {
                console.error('❌ Google giriş hatası:', error);
                currentUserEmail = null;
                
                if (error.code === 'auth/popup-closed-by-user') {
                    showMessage('Google giriş penceresi kapatıldı.', 'error');
                } else if (error.code === 'auth/popup-blocked') {
                    showMessage('Popup engellenmiş! Tarayıcınızın popup ayarlarını kontrol edin.', 'error');
                } else {
                    showMessage('Google girişi başarısız: ' + error.message, 'error');
                }
            }
        }

        // Google ile Giriş (disclaimer kabul edildikten sonra)
        async function signInWithGoogle() {
            try {
                const provider = new firebase.auth.GoogleAuthProvider();
                provider.addScope('email');
                provider.addScope('profile');
                
                console.log('🔐 Google ile giriş yapılıyor...');
                
                const result = await auth.signInWithPopup(provider);
                firebaseAuthUser = result.user;
                window.googleUser = result.user; // Global olarak sakla
                
                console.log('✅ Google girişi başarılı!');
                console.log('Kullanıcı:', firebaseAuthUser.displayName);
                console.log('Email:', firebaseAuthUser.email);
                console.log('UID:', firebaseAuthUser.uid);
                
                // Görsel bildirim göster
                showAuthStatus(firebaseAuthUser.email, 'Google');
                
                // Form butonlarını aktif et
                enableLoginButtons();
                
                // Kullanıcının sistemde kayıtlı olup olmadığını kontrol et
                allUsers = await firebaseDB.getAll();
                const existingUser = allUsers.find(u => u.google_email === firebaseAuthUser.email);
                
                if (existingUser) {
                    // Kullanıcı kayıtlı, normal giriş ekranına yönlendir
                    showMessage(`Merhaba ${firebaseAuthUser.displayName}! Lütfen rumuz ve şifrenizle giriş yapın.`, 'success');
                    // Giriş ekranında kal
                } else {
                    // Kullanıcı kayıtlı değil, kayıt ekranına yönlendir
                    showMessage(`Merhaba ${firebaseAuthUser.displayName}! Lütfen kayıt formunu doldurun.`, 'success');
                    showRegister();
                    
                    // Google bilgilerini kayıt formunda göster
                    const googleAuthInfo = document.getElementById('googleAuthInfo');
                    const registerGoogleEmail = document.getElementById('registerGoogleEmail');
                    
                    if (googleAuthInfo && registerGoogleEmail) {
                        googleAuthInfo.style.display = 'block';
                        registerGoogleEmail.textContent = firebaseAuthUser.email;
                    }
                }
                
                // Analytics event
                firebase.analytics().logEvent('login', {
                    method: 'Google'
                });
                
            } catch (error) {
                console.error('❌ Google giriş hatası:', error);
                
                if (error.code === 'auth/popup-closed-by-user') {
                    showMessage('Google giriş penceresi kapatıldı.', 'error');
                } else if (error.code === 'auth/popup-blocked') {
                    showMessage('Popup engellenmiş! Tarayıcınızın popup ayarlarını kontrol edin.', 'error');
                } else {
                    showMessage('Google girişi başarısız: ' + error.message, 'error');
                }
            }
        }

        // Auth Status'u göster
        function showAuthStatus(email, method) {
            const statusBox = document.getElementById('firebaseAuthStatus');
            const emailDisplay = document.getElementById('authEmailDisplay');
            const methodText = document.getElementById('authMethodText');
            const googleBtn = document.getElementById('googleLoginBtn');
            const disclaimerBtn = document.getElementById('disclaimerBtn');
            
            emailDisplay.textContent = email || 'Anonim Kullanıcı';
            methodText.textContent = 'Giriş Yapıldı ✓';
            
            // Google butonunu yeşil yap ve email göster
            if (googleBtn) {
                googleBtn.style.background = 'linear-gradient(135deg, #4caf50 0%, #45a049 100%)';
                googleBtn.style.borderColor = 'rgba(255, 255, 255, 0.5)';
                googleBtn.innerHTML = `
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" width="24px" height="24px">
                        <path fill="#4caf50" d="M44,24c0,11.045-8.955,20-20,20S4,35.045,4,24S12.955,4,24,4S44,12.955,44,24z"/>
                        <path fill="#fff" d="M34.586,14.586l-13.57,13.586l-5.602-5.586l-2.828,2.828l8.434,8.414l16.395-16.414L34.586,14.586z"/>
                    </svg>
                    <span style="flex: 1; text-align: left;">${email}</span>
                `;
                googleBtn.style.cursor = 'default';
                googleBtn.onclick = null;
            }
            
            // Sorumluluk reddi butonunu yeşil yap
            if (disclaimerBtn) {
                disclaimerBtn.style.background = 'linear-gradient(135deg, #4caf50 0%, #45a049 100%)';
                disclaimerBtn.style.boxShadow = '0 4px 15px rgba(76, 175, 80, 0.3)';
            }
        }

        // Giriş butonlarını aktif et
        function enableLoginButtons() {
            // Input alanlarını aktif et
            document.getElementById('loginNickname').disabled = false;
            document.getElementById('loginPassword').disabled = false;
            
            // Giriş Yap butonunu aktif et
            const loginBtn = document.getElementById('loginBtn');
            loginBtn.disabled = false;
            loginBtn.style.opacity = '1';
            loginBtn.style.cursor = 'pointer';
            
            // Üye Ol butonunu aktif et
            const registerBtn = document.getElementById('registerBtn');
            registerBtn.disabled = false;
            registerBtn.style.opacity = '1';
            registerBtn.style.cursor = 'pointer';
            
            // Bilgi metnini gizle
            const infoText = document.querySelector('#loginForm p');
            if (infoText) {
                infoText.style.display = 'none';
            }
        }

        // Giriş butonlarını devre dışı bırak
        function disableLoginButtons() {
            // Input alanlarını devre dışı bırak
            document.getElementById('loginNickname').disabled = true;
            document.getElementById('loginPassword').disabled = true;
            
            // Giriş Yap butonunu devre dışı bırak
            const loginBtn = document.getElementById('loginBtn');
            loginBtn.disabled = true;
            loginBtn.style.opacity = '0.5';
            loginBtn.style.cursor = 'not-allowed';
            
            // Üye Ol butonunu devre dışı bırak
            const registerBtn = document.getElementById('registerBtn');
            registerBtn.disabled = true;
            registerBtn.style.opacity = '0.5';
            registerBtn.style.cursor = 'not-allowed';
            
            // Bilgi metnini göster
            const infoText = document.querySelector('#loginForm p');
            if (infoText) {
                infoText.style.display = 'block';
            }
        }

        // Auth Status'u kapat
        function closeAuthStatus() {
            const statusBox = document.getElementById('firebaseAuthStatus');
            const googleBtn = document.getElementById('googleLoginBtn');
            
            statusBox.classList.add('hidden');
            // Butonu tekrar göster
            if (googleBtn) {
                googleBtn.style.display = 'flex';
            }
            
            // Giriş butonlarını devre dışı bırak
            disableLoginButtons();
        }

        // Firebase Anonymous Authentication - Otomatik giriş
        async function ensureFirebaseAuth() {
            if (firebaseAuthUser) {
                return firebaseAuthUser;
            }

            try {
                // Mevcut kullanıcıyı kontrol et
                if (auth.currentUser) {
                    firebaseAuthUser = auth.currentUser;
                    console.log('🔐 Firebase Auth - Mevcut kullanıcı:', firebaseAuthUser.uid);
                    
                    // Eğer Google ile giriş yapılmışsa göster ve butonları aktif et
                    if (firebaseAuthUser.email) {
                        showAuthStatus(firebaseAuthUser.email, 'Google');
                        enableLoginButtons();
                    }
                    
                    return firebaseAuthUser;
                }

                // Anonim giriş yapmıyoruz - sadece database erişimi için gerekli değil
                console.log('⚠️ Firebase Auth - Kullanıcı giriş yapmamış, database sadece okuma modunda.');
                return null;
            } catch (error) {
                console.error('❌ Firebase Auth hatası:', error);
                throw error;
            }
        }

        // Firebase Realtime Database Yönetimi
        const firebaseDB = {
            // Tüm kullanıcıları getir
            async getAll() {
                try {
                    await ensureFirebaseAuth(); // Auth kontrolü
                    const snapshot = await database.ref('users').once('value');
                    const usersObj = snapshot.val() || {};
                    return Object.values(usersObj);
                } catch (error) {
                    console.error('Kullanıcılar getirilemedi:', error);
                    return [];
                }
            },
            
            // Yeni kullanıcı ekle
            async create(user) {
                try {
                    await ensureFirebaseAuth(); // Auth kontrolü
                    console.log('Firebase\'e kullanıcı kaydediliyor:', user.nickname);
                    await database.ref('users/' + user.user_id).set(user);
                    console.log('✅ Firebase\'e başarıyla kaydedildi!');
                    return { isOk: true, data: user };
                } catch (error) {
                    console.error('❌ Firebase kayıt hatası:', error);
                    console.error('Hata detayı:', error.code, error.message);
                    return { isOk: false, error: error.message };
                }
            },
            
            // Kullanıcı güncelle
            async update(updatedUser) {
                try {
                    await ensureFirebaseAuth(); // Auth kontrolü
                    await database.ref('users/' + updatedUser.user_id).update(updatedUser);
                    return { isOk: true, data: updatedUser };
                } catch (error) {
                    console.error('Kullanıcı güncellenemedi:', error);
                    return { isOk: false, error: error.message };
                }
            },
            
            // Kullanıcı sil
            async delete(userId) {
                try {
                    await ensureFirebaseAuth(); // Auth kontrolü
                    await database.ref('users/' + userId).remove();
                    return { isOk: true };
                } catch (error) {
                    console.error('Kullanıcı silinemedi:', error);
                    return { isOk: false, error: error.message };
                }
            },

            // Kullanıcı ID'sine göre getir
            async getById(userId) {
                try {
                    await ensureFirebaseAuth(); // Auth kontrolü
                    const snapshot = await database.ref('users/' + userId).once('value');
                    return snapshot.val();
                } catch (error) {
                    console.error('Kullanıcı bulunamadı:', error);
                    return null;
                }
            },

            // Rumuz ve telefona göre kullanıcı bul
            async findByNicknameAndPhone(nickname, phone) {
                try {
                    await ensureFirebaseAuth(); // Auth kontrolü
                    const snapshot = await database.ref('users').once('value');
                    const usersObj = snapshot.val() || {};
                    const users = Object.values(usersObj);
                    // Büyük/küçük harf duyarsız rumuz karşılaştırması
                    return users.find(u => u.nickname.toLowerCase() === nickname.toLowerCase() && (!phone || u.phone === phone));
                } catch (error) {
                    console.error('Kullanıcı araması başarısız:', error);
                    return null;
                }
            }
        };

        // Sayfa yüklendiğinde kullanıcıları yükle
        async function initializeApp() {
            try {
                console.log('🔥 Firebase bağlantısı başlatılıyor...');
                console.log('Database URL:', database.ref().toString());
                
                // Önce anonim authentication yap
                await ensureFirebaseAuth();
                
                allUsers = await firebaseDB.getAll();
                console.log('✅ Firebase bağlantısı başarılı! Toplam kullanıcı:', allUsers.length);
                
                // Eğer ilk kullanımsa bilgilendirme göster
                if (allUsers.length === 0) {
                    console.log('ℹ️ Henüz kullanıcı yok. İlk kaydınızı oluşturabilirsiniz.');
                }
            } catch (error) {
                console.error('❌ Firebase başlatma hatası:', error);
                console.error('Hata kodu:', error.code);
                console.error('Hata mesajı:', error.message);
                
                if (error.code === "auth/operation-not-allowed") {
                    console.error('');
                    console.error('� Firebase Anonymous Authentication aktif değil!');
                    console.error('');
                    console.error('Firebase Console\'a gidin:');
                    console.error('1. https://console.firebase.google.com/');
                    console.error('2. "kariyer-gelisimi" projesini seçin');
                    console.error('3. Authentication > Sign-in method');
                    console.error('4. "Anonymous" seçeneğini aktif edin (Enable)');
                    console.error('5. "Save" butonuna tıklayın');
                    console.error('');
                    console.error('Database Rules zaten doğru (auth != null)');
                    console.error('Sadece Anonymous Authentication\'ı açmanız yeterli!');
                    console.error('');
                }
                
                if (error.code === "PERMISSION_DENIED" || error.message.includes("permission")) {
                    console.error('');
                    console.error('🔒 Firebase Database Rules doğru!');
                    console.error('Rules: auth != null (Kimlik doğrulama gerekli)');
                    console.error('');
                    console.error('Şimdi Anonymous Authentication\'ı aktif edin:');
                    console.error('1. https://console.firebase.google.com/');
                    console.error('2. Authentication > Sign-in method');
                    console.error('3. "Anonymous" seçeneğini ENABLE yapın');
                    console.error('');
                }
            }
        }

        // Sayfa yüklendiğinde SDK'ları başlat
        document.addEventListener('DOMContentLoaded', initializeApp);
        // Backup olarak hemen de başlat
        if (document.readyState === 'loading') {
            document.addEventListener('DOMContentLoaded', initializeApp);
        } else {
            initializeApp();
        }

        // Şifre üretici
        function generatePassword() {
            const upperChars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
            const lowerChars = 'abcdefghijklmnopqrstuvwxyz';
            const numbers = '0123456789';
            const allChars = upperChars + lowerChars + numbers;
            
            let password = '';
            
            // En az bir büyük harf
            password += upperChars.charAt(Math.floor(Math.random() * upperChars.length));
            
            // En az bir küçük harf
            password += lowerChars.charAt(Math.floor(Math.random() * lowerChars.length));
            
            // En az bir rakam
            password += numbers.charAt(Math.floor(Math.random() * numbers.length));
            
            // Kalan 3 karakter rastgele
            for (let i = 0; i < 3; i++) {
                password += allChars.charAt(Math.floor(Math.random() * allChars.length));
            }
            
            // Karakterleri karıştır (shuffle)
            password = password.split('').sort(() => Math.random() - 0.5).join('');
            
            return password;
        }

        // Kayıt işlemi
        async function handleRegister(event) {
            event.preventDefault();
            
            // Form verilerini kontrol et
            const nickname = document.getElementById('nickname').value.trim();
            const phone = document.getElementById('phone').value.trim();
            const education = document.getElementById('education').value;
            const department = document.getElementById('department').value.trim();
            const position = document.getElementById('position').value.trim();

            // Boş alan kontrolü
            if (!nickname || !phone || !education || !department || !position) {
                showMessage("Lütfen tüm alanları doldurun.", "error");
                return;
            }

            // Telefon numarası formatı kontrolü
            if (phone.length < 10) {
                showMessage("Lütfen geçerli bir telefon numarası girin.", "error");
                return;
            }

            if (allUsers.length >= 999) {
                showMessage("Maksimum 999 üye limitine ulaşıldı. Yeni kayıt yapılamaz.", "error");
                return;
            }

            const btn = document.getElementById('submitRegisterBtn');
            if (!btn) {
                showMessage("Kayıt butonu bulunamadı!", "error");
                return;
            }
            const btnText = btn.querySelector('.btn-text');
            const loading = btn.querySelector('.loading');
            
            btnText.classList.add('hidden');
            loading.classList.remove('hidden');
            btn.disabled = true;

            try {
                // Rumuz kontrolü (Firebase'den)
                const existingUser = await firebaseDB.findByNicknameAndPhone(nickname, null);
                if (existingUser) {
                    showMessage("Bu rumuz zaten kullanılıyor. Lütfen farklı bir rumuz seçin.", "error");
                    btnText.classList.remove('hidden');
                    loading.classList.add('hidden');
                    btn.disabled = false;
                    return;
                }

                const formData = {
                    user_id: Date.now().toString(),
                    nickname: nickname,
                    phone: phone,
                    education_level: education,
                    department: department,
                    current_position: position,
                    password: generatePassword(),
                    registration_date: new Date().toISOString(),
                    test_completed: false,
                    test_date: "",
                    test_results: "",
                    overall_score: 0,
                    test_history: [],
                    is_active: true,
                    google_email: firebaseAuthUser && firebaseAuthUser.email ? firebaseAuthUser.email : null,
                    google_name: firebaseAuthUser && firebaseAuthUser.displayName ? firebaseAuthUser.displayName : null
                };

                console.log('📝 Kayıt verisi hazırlandı:', formData.nickname);

                // Firebase'e kaydet
                const result = await firebaseDB.create(formData);
                
                console.log('📡 Firebase yanıtı:', result);
                
                btnText.classList.remove('hidden');
                loading.classList.add('hidden');
                btn.disabled = false;

                if (result.isOk) {
                    // Kullanıcı listesini güncelle
                    allUsers = await firebaseDB.getAll();
                    
                    console.log('✅ Kullanıcı başarıyla kaydedildi! Toplam kullanıcı:', allUsers.length);
                    
                    // Başarı mesajı
                    showMessage("Kayıt başarılı! Şifrenizi almak için lütfen süper yönetici ile iletişime geçin.", "success");
                    
                    // LinkedIn yönlendirme onayı
                    setTimeout(() => {
                        const confirmDiv = document.createElement('div');
                        confirmDiv.style.cssText = `
                            position: fixed;
                            top: 50%;
                            left: 50%;
                            transform: translate(-50%, -50%);
                            background: white;
                            padding: 30px;
                            border-radius: 15px;
                            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
                            z-index: 10001;
                            text-align: center;
                            max-width: 400px;
                        `;
                        confirmDiv.innerHTML = `
                            <h3 style="margin-bottom: 15px; color: #667eea;">Şifre Alma</h3>
                            <p style="margin-bottom: 20px;">Şifrenizi almak için LinkedIn bağlantısına tıklayarak süper yönetici ile iletişime geçmeniz gerekiyor.</p>
                            <p style="margin-bottom: 25px;"><strong>Şimdi LinkedIn sayfasını açmak istiyor musunuz?</strong></p>
                            <button onclick="window.open('https://www.linkedin.com/in/bar%C4%B1%C5%9F-ak%C3%A7a-46997593/', '_blank'); document.body.removeChild(this.parentElement);" 
                                    style="background: #0077b5; color: white; border: none; padding: 12px 25px; border-radius: 8px; margin: 5px; cursor: pointer;">
                                LinkedIn'i Aç
                            </button>
                            <button onclick="document.body.removeChild(this.parentElement);" 
                                    style="background: #6c757d; color: white; border: none; padding: 12px 25px; border-radius: 8px; margin: 5px; cursor: pointer;">
                                Daha Sonra
                            </button>
                        `;
                        document.body.appendChild(confirmDiv);
                    }, 1000);
                    
                    document.getElementById('registerForm').reset();
                    setTimeout(() => showLogin(), 3000);
                } else {
                    console.error("❌ Kayıt hatası:", result.error);
                    
                    // Kullanıcıya anlaşılır hata mesajı
                    let errorMessage = "Kayıt sırasında hata oluştu.";
                    
                    if (result.error && result.error.includes("permission")) {
                        errorMessage = "🔒 Firebase veritabanı izinleri ayarlanmamış! Lütfen Firebase Console'dan Database Rules'u ayarlayın.";
                    } else if (result.error) {
                        errorMessage = `Hata: ${result.error}`;
                    }
                    
                    showMessage(errorMessage, "error");
                }
            } catch (error) {
                console.error("❌ Kayıt işlemi hatası:", error);
                
                let errorMessage = "Sistem hatası oluştu.";
                
                if (error.code === "PERMISSION_DENIED") {
                    errorMessage = "🔒 Firebase veritabanı izinleri ayarlanmamış! Lütfen Firebase Console'dan Database Rules'u ayarlayın.";
                } else if (error.message) {
                    errorMessage = `Hata: ${error.message}`;
                }
                
                showMessage(errorMessage, "error");
                
                btnText.classList.remove('hidden');
                loading.classList.add('hidden');
                btn.disabled = false;
            }
        }

        // Giriş işlemi
        async function handleLogin(event) {
            event.preventDefault();
            
            const btn = document.getElementById('loginBtn');
            const btnText = btn.querySelector('.btn-text');
            const loading = btn.querySelector('.loading');
            
            btnText.classList.add('hidden');
            loading.classList.remove('hidden');
            btn.disabled = true;

            const nickname = document.getElementById('loginNickname').value.trim();
            const password = document.getElementById('loginPassword').value.trim();

            console.log('Giriş denemesi - Rumuz:', nickname);
            
            try {
                // Firebase'den tüm kullanıcıları güncelle
                allUsers = await firebaseDB.getAll();
                console.log('Toplam kullanıcı sayısı:', allUsers.length);
                
                const user = allUsers.find(u => {
                    console.log('Kontrol ediliyor:', u.nickname, '===', nickname);
                    // Büyük/küçük harf duyarsız rumuz karşılaştırması
                    return u.nickname.toLowerCase() === nickname.toLowerCase() && u.password === password;
                });
                
                btnText.classList.remove('hidden');
                loading.classList.add('hidden');
                btn.disabled = false;

                if (user) {
                    // Kullanıcı aktif mi kontrol et
                    const isActive = user.is_active === undefined ? true : user.is_active;
                    
                    if (!isActive) {
                        console.log('Giriş reddedildi - Kullanıcı pasif');
                        showMessage("Hesabınız pasif durumda! Lütfen yönetici ile iletişime geçin.", "error");
                        return;
                    }
                    
                    currentUser = user;
                    console.log('Giriş başarılı:', user);
                    showWelcome();
                } else {
                    console.log('Giriş başarısız - Kullanıcı bulunamadı');
                    showMessage("Rumuz veya şifre hatalı!", "error");
                }
            } catch (error) {
                console.error('Giriş hatası:', error);
                showMessage("Giriş sırasında bir hata oluştu. Lütfen tekrar deneyin.", "error");
                
                btnText.classList.remove('hidden');
                loading.classList.add('hidden');
                btn.disabled = false;
            }
        }

        // Admin giriş
        // Admin giriş
        function showAdminLogin() {
            hideAllScreens();
            document.getElementById('adminLoginScreen').classList.remove('hidden');
            
            // Eğer Google ile giriş yapılmışsa formu göster
            if (firebaseAuthUser && firebaseAuthUser.email) {
                document.getElementById('adminGoogleAuthStatus').style.display = 'block';
                document.getElementById('adminGoogleEmail').textContent = firebaseAuthUser.email;
                document.getElementById('adminGoogleBtn').style.display = 'none';
                document.getElementById('adminLoginForm').style.display = 'block';
            } else {
                document.getElementById('adminGoogleAuthStatus').style.display = 'none';
                document.getElementById('adminGoogleBtn').style.display = 'flex';
                document.getElementById('adminLoginForm').style.display = 'none';
            }
        }

        // Admin için Google Login
        async function adminGoogleLogin() {
            try {
                const provider = new firebase.auth.GoogleAuthProvider();
                provider.addScope('email');
                provider.addScope('profile');
                
                console.log('🔐 Admin - Google ile giriş yapılıyor...');
                
                const result = await auth.signInWithPopup(provider);
                firebaseAuthUser = result.user;
                window.googleUser = result.user; // Global olarak sakla
                
                console.log('✅ Admin Google girişi başarılı!');
                console.log('Admin:', firebaseAuthUser.displayName);
                console.log('Email:', firebaseAuthUser.email);
                
                // SÜPER ADMIN KONTROLÜ
                if (firebaseAuthUser.email !== SUPER_ADMIN_EMAIL) {
                    console.warn('⚠️ Yetkisiz admin girişi denemesi:', firebaseAuthUser.email);
                    
                    // Oturumu kapat
                    await auth.signOut();
                    firebaseAuthUser = null;
                    window.googleUser = null;
                    
                    showMessage(`❌ Admin paneline erişim yetkiniz yok!\n\nSadece "${SUPER_ADMIN_EMAIL}" hesabı admin paneline erişebilir.`, 'error');
                    
                    // Analytics - Yetkisiz giriş denemesi
                    firebase.analytics().logEvent('unauthorized_admin_attempt', {
                        attempted_email: result.user.email,
                        timestamp: new Date().toISOString()
                    });
                    
                    return;
                }
                
                // Admin bilgilerini göster
                document.getElementById('adminGoogleAuthStatus').style.display = 'block';
                document.getElementById('adminGoogleEmail').textContent = firebaseAuthUser.email;
                document.getElementById('adminGoogleBtn').style.display = 'none';
                document.getElementById('adminLoginForm').style.display = 'block';
                
                showMessage(`✅ Merhaba ${firebaseAuthUser.displayName}! Şimdi admin şifrenizi girin.`, 'success');
                
                // Analytics
                firebase.analytics().logEvent('admin_google_login', {
                    email: firebaseAuthUser.email
                });
                
            } catch (error) {
                console.error('❌ Admin Google giriş hatası:', error);
                
                if (error.code === 'auth/popup-closed-by-user') {
                    showMessage('Google giriş penceresi kapatıldı.', 'error');
                } else if (error.code === 'auth/popup-blocked') {
                    showMessage('Popup engellenmiş! Tarayıcınızın popup ayarlarını kontrol edin.', 'error');
                } else {
                    showMessage('Google girişi başarısız: ' + error.message, 'error');
                }
            }
        }

        // Admin giriş işlemi
        function handleAdminLogin(event) {
            event.preventDefault();
            
            // Google authentication kontrolü
            if (!firebaseAuthUser || !firebaseAuthUser.email) {
                showMessage("⚠️ Önce Google ile kimlik doğrulaması yapmalısınız!", "error");
                return;
            }
            
            // SÜPER ADMIN EMAIL KONTROLÜ (Ekstra güvenlik katmanı)
            if (firebaseAuthUser.email !== SUPER_ADMIN_EMAIL) {
                showMessage(`❌ Yetkisiz erişim!\n\nSadece "${SUPER_ADMIN_EMAIL}" hesabı admin paneline erişebilir.`, "error");
                
                // Analytics - Yetkisiz giriş denemesi
                firebase.analytics().logEvent('unauthorized_admin_password_attempt', {
                    email: firebaseAuthUser.email,
                    timestamp: new Date().toISOString()
                });
                
                // Güvenlik için oturumu kapat
                auth.signOut();
                firebaseAuthUser = null;
                window.googleUser = null;
                hideAdminLogin();
                return;
            }
            
            const password = document.getElementById('adminPassword').value;
            
            if (password === "030714") {
                console.log('✅ Admin panel erişimi:', firebaseAuthUser.email);
                
                // Analytics - Admin paneline giriş
                firebase.analytics().logEvent('admin_panel_access', {
                    email: firebaseAuthUser.email,
                    timestamp: new Date().toISOString()
                });
                
                showAdminPanel();
            } else {
                showMessage("Hatalı admin şifresi!", "error");
                document.getElementById('adminPassword').value = '';
                
                // Analytics - Başarısız giriş denemesi
                firebase.analytics().logEvent('admin_login_failed', {
                    email: firebaseAuthUser.email
                });
            }
        }

        // Admin giriş ekranını gizle
        // Admin giriş ekranını gizle
        function hideAdminLogin() {
            document.getElementById('adminLoginScreen').classList.add('hidden');
            document.getElementById('adminPassword').value = ''; // Şifreyi temizle
            showLogin();
        }

        // Admin panel göster
        async function showAdminPanel() {
            hideAllScreens();
            document.getElementById('adminPanel').classList.remove('hidden');
            await updateAdminPanel();
        }

        // Üye silme fonksiyonu
        async function deleteUser(userId, nickname) {
            if (confirm(`"${nickname}" kullanıcısını silmek istediğinizden emin misiniz?\n\nBu işlem geri alınamaz!`)) {
                const result = await firebaseDB.delete(userId);
                if (result.isOk) {
                    showMessage(`"${nickname}" başarıyla silindi.`, "success");
                    allUsers = await firebaseDB.getAll();
                    await updateAdminPanel();
                } else {
                    showMessage("Kullanıcı silinirken hata oluştu!", "error");
                }
            }
        }

        // Üye aktif/pasif yapma
        async function toggleUserStatus(userId) {
            const user = await firebaseDB.getById(userId);
            
            if (user) {
                user.is_active = user.is_active === undefined ? false : !user.is_active;
                
                const result = await firebaseDB.update(user);
                if (result.isOk) {
                    const status = user.is_active ? 'aktif' : 'pasif';
                    showMessage(`"${user.nickname}" ${status} yapıldı.`, "success");
                    allUsers = await firebaseDB.getAll();
                    await updateAdminPanel();
                } else {
                    showMessage("Durum değiştirilemedi!", "error");
                }
            }
        }

        // Kullanıcıları filtreleme ve sıralama için değişkenler
        let filteredUsers = [];
        let sortOrder = 'asc'; // 'asc' veya 'desc'
        let sortColumn = 'nickname'; // varsayılan sıralama kolonu

        // Kullanıcıları filtrele
        function filterUsers() {
            const searchInput = document.getElementById('adminSearchInput');
            const searchTerm = searchInput.value.toLowerCase().trim();
            
            if (searchTerm === '') {
                filteredUsers = [...allUsers];
            } else {
                filteredUsers = allUsers.filter(user => 
                    user.nickname.toLowerCase().includes(searchTerm) ||
                    user.phone.includes(searchTerm) ||
                    user.department.toLowerCase().includes(searchTerm) ||
                    user.current_position.toLowerCase().includes(searchTerm)
                );
            }
            
            renderAdminTable();
        }

        // Kullanıcıları sırala
        function sortUsers(column) {
            // Aynı kolona tıklanırsa sıralama yönünü değiştir
            if (sortColumn === column) {
                sortOrder = sortOrder === 'asc' ? 'desc' : 'asc';
            } else {
                sortColumn = column;
                sortOrder = 'asc';
            }

            filteredUsers.sort((a, b) => {
                let aVal = a[column];
                let bVal = b[column];

                // Tarih alanları için özel işlem
                if (column === 'registration_date' || column === 'test_date') {
                    aVal = new Date(aVal || 0).getTime();
                    bVal = new Date(bVal || 0).getTime();
                }
                // Sayısal alanlar için
                else if (column === 'overall_score') {
                    aVal = parseFloat(aVal || 0);
                    bVal = parseFloat(bVal || 0);
                }
                // Metin alanları için
                else {
                    aVal = String(aVal || '').toLowerCase();
                    bVal = String(bVal || '').toLowerCase();
                }

                if (sortOrder === 'asc') {
                    return aVal > bVal ? 1 : aVal < bVal ? -1 : 0;
                } else {
                    return aVal < bVal ? 1 : aVal > bVal ? -1 : 0;
                }
            });

            renderAdminTable();
        }

        // Admin tablosunu render et
        function renderAdminTable() {
            const content = document.getElementById('adminContent');
            
            if (filteredUsers.length === 0) {
                const searchInput = document.getElementById('adminSearchInput');
                if (searchInput && searchInput.value.trim() !== '') {
                    content.innerHTML = `
                        <div class="admin-controls">
                            <input type="text" id="adminSearchInput" placeholder="İsim, telefon, bölüm veya pozisyon ile ara..." 
                                   onkeyup="filterUsers()" style="width: 100%; padding: 10px; margin-bottom: 15px; border: 2px solid #ddd; border-radius: 8px; font-size: 14px;">
                        </div>
                        <p>Arama sonucu bulunamadı.</p>
                    `;
                } else {
                    content.innerHTML = '<p>Henüz kayıtlı üye bulunmuyor.</p>';
                }
                return;
            }

            let html = `
                <div class="admin-controls" style="margin-bottom: 15px;">
                    <input type="text" id="adminSearchInput" placeholder="İsim, telefon, bölüm veya pozisyon ile ara..." 
                           onkeyup="filterUsers()" style="width: 100%; padding: 10px; margin-bottom: 10px; border: 2px solid #ddd; border-radius: 8px; font-size: 14px;">
                    <div style="display: flex; gap: 10px; align-items: center;">
                        <span style="font-weight: bold;">Toplam Üye: ${allUsers.length}</span>
                        <span style="color: #666;">|</span>
                        <span>Gösterilen: ${filteredUsers.length}</span>
                    </div>
                </div>
                <div style="overflow-x: auto;">
                <table class="admin-table" style="width: 100%; border-collapse: collapse;">
                    <thead>
                        <tr style="background: linear-gradient(135deg, #667eea, #764ba2); color: white;">
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('nickname')">
                                Rumuz ${sortColumn === 'nickname' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('phone')">
                                Telefon ${sortColumn === 'phone' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('education_level')">
                                Mezuniyet ${sortColumn === 'education_level' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('department')">
                                Bölüm ${sortColumn === 'department' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('current_position')">
                                Pozisyon ${sortColumn === 'current_position' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="padding: 12px; text-align: left;">Şifre</th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('registration_date')">
                                Kayıt Tarihi ${sortColumn === 'registration_date' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('test_completed')">
                                Test Durumu ${sortColumn === 'test_completed' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('test_date')">
                                Test Tarihi ${sortColumn === 'test_date' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('overall_score')">
                                Genel Skor ${sortColumn === 'overall_score' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="cursor: pointer; padding: 12px; text-align: left;" onclick="sortUsers('is_active')">
                                Durum ${sortColumn === 'is_active' ? (sortOrder === 'asc' ? '↑' : '↓') : ''}
                            </th>
                            <th style="padding: 12px; text-align: center;">İşlemler</th>
                        </tr>
                    </thead>
                    <tbody>
            `;

            filteredUsers.forEach(user => {
                const registrationDate = new Date(user.registration_date).toLocaleDateString('tr-TR');
                const testDate = user.test_date ? new Date(user.test_date).toLocaleDateString('tr-TR') : '-';
                const testStatus = user.test_completed ? 'Tamamlandı' : 'Bekliyor';
                const isActive = user.is_active === undefined ? true : user.is_active;
                const statusText = isActive ? 'Aktif' : 'Pasif';
                const statusColor = isActive ? 'green' : 'red';
                const toggleBtnText = isActive ? 'Pasif Yap' : 'Aktif Yap';
                
                html += `
                    <tr style="${!isActive ? 'opacity: 0.6; background: #fff3cd;' : 'background: white;'} border-bottom: 1px solid #eee;">
                        <td style="padding: 10px;">${user.nickname}</td>
                        <td style="padding: 10px;">${user.phone}</td>
                        <td style="padding: 10px;">${user.education_level}</td>
                        <td style="padding: 10px;">${user.department}</td>
                        <td style="padding: 10px;">${user.current_position}</td>
                        <td style="padding: 10px;"><strong>${user.password}</strong></td>
                        <td style="padding: 10px;">${registrationDate}</td>
                        <td style="padding: 10px;">${testStatus}</td>
                        <td style="padding: 10px;">${testDate}</td>
                        <td style="padding: 10px;"><strong>${user.overall_score}%</strong></td>
                        <td style="padding: 10px;"><strong style="color: ${statusColor};">${statusText}</strong></td>
                        <td style="padding: 10px; text-align: center;">
                            <button onclick="toggleUserStatus('${user.user_id}')" 
                                    style="padding: 5px 10px; margin: 2px; background: #ffc107; color: #000; border: none; border-radius: 4px; cursor: pointer; font-size: 12px;">
                                ${toggleBtnText}
                            </button>
                            <button onclick="deleteUser('${user.user_id}', '${user.nickname}')" 
                                    style="padding: 5px 10px; margin: 2px; background: #dc3545; color: white; border: none; border-radius: 4px; cursor: pointer; font-size: 12px;">
                                Sil
                            </button>
                        </td>
                    </tr>
                `;
            });

            html += '</tbody></table></div>';
            content.innerHTML = html;
            
            // Arama inputuna mevcut değeri geri yükle
            const searchInput = document.getElementById('adminSearchInput');
            if (searchInput && typeof filterUsers.lastSearch !== 'undefined') {
                searchInput.value = filterUsers.lastSearch;
            }
        }

        // Admin panel güncelle
        async function updateAdminPanel() {
            const content = document.getElementById('adminContent');
            
            // Firebase'den güncel verileri çek
            allUsers = await firebaseDB.getAll();
            
            if (allUsers.length === 0) {
                content.innerHTML = '<p>Henüz kayıtlı üye bulunmuyor.</p>';
                return;
            }

            // Filtrelenmiş listeyi başlat
            filteredUsers = [...allUsers];
            
            // Tabloyu render et
            renderAdminTable();
        }

        // Ekran yönetimi
        function hideAllScreens() {
            document.getElementById('loginScreen').classList.add('hidden');
            document.getElementById('registerScreen').classList.add('hidden');
            document.getElementById('welcomeScreen').classList.add('hidden');
            document.getElementById('quizContainer').style.display = 'none';
            document.getElementById('resultsContainer').style.display = 'none';
            document.getElementById('reportContainer').style.display = 'none';
            document.getElementById('myReportsScreen').classList.add('hidden');
            document.getElementById('adminLoginScreen').classList.add('hidden');
            document.getElementById('adminPanel').classList.add('hidden');
        }

        function showLogin() {
            hideAllScreens();
            document.getElementById('loginScreen').classList.remove('hidden');
        }

        function showRegister() {
            hideAllScreens();
            document.getElementById('registerScreen').classList.remove('hidden');
        }

        function showWelcome() {
            hideAllScreens();
            document.getElementById('welcomeScreen').classList.remove('hidden');
        }

        function hideAdmin() {
            document.getElementById('adminPanel').classList.add('hidden');
            document.getElementById('adminPassword').value = ''; // Şifreyi temizle
            showLogin();
        }

        function logout() {
            currentUser = null;
            showLogin();
        }

        function backToWelcome() {
            // Dinamik olarak oluşturulmuş ekranları kaldır
            const progressChart = document.getElementById('progressChartScreen');
            if (progressChart) progressChart.remove();
            
            const comparisonScreen = document.getElementById('comparisonScreen');
            if (comparisonScreen) comparisonScreen.remove();
            
            document.getElementById('resultsContainer').style.display = 'none';
            document.getElementById('reportContainer').style.display = 'none';
            showWelcome();
        }

        function backToWelcomeFromReports() {
            // Dinamik olarak oluşturulmuş ekranları kaldır
            const progressChart = document.getElementById('progressChartScreen');
            if (progressChart) progressChart.remove();
            
            const comparisonScreen = document.getElementById('comparisonScreen');
            if (comparisonScreen) comparisonScreen.remove();
            
            document.getElementById('myReportsScreen').classList.add('hidden');
            showWelcome();
        }

        function showMyReports() {
            // Dinamik olarak oluşturulmuş ekranları kaldır
            const progressChart = document.getElementById('progressChartScreen');
            if (progressChart) progressChart.remove();
            
            const comparisonScreen = document.getElementById('comparisonScreen');
            if (comparisonScreen) comparisonScreen.remove();
            
            hideAllScreens();
            document.getElementById('myReportsScreen').classList.remove('hidden');
            loadReportsHistory();
        }

        function loadReportsHistory() {
            const container = document.getElementById('reportsHistory');
            
            if (!currentUser || !currentUser.test_history || currentUser.test_history.length === 0) {
                container.innerHTML = `
                    <div style="text-align: center; padding: 40px; color: #999;">
                        <p style="font-size: 18px;">📭 Henüz test geçmişiniz bulunmuyor.</p>
                        <p>Envanter testini tamamladıktan sonra sonuçlarınızı burada görebilirsiniz.</p>
                    </div>
                `;
                return;
            }

            let html = '<div style="display: grid; gap: 20px;">';
            
            // Tüm Zamanlar Ortalaması Kartı
            if (currentUser.test_history.length > 1) {
                const avgScore = Math.round(
                    currentUser.test_history.reduce((sum, test) => sum + test.overall_score, 0) / 
                    currentUser.test_history.length
                );
                
                html += `
                    <div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 15px; padding: 25px; box-shadow: 0 4px 20px rgba(102, 126, 234, 0.4); color: white;">
                        <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 15px;">
                            <div>
                                <h3 style="margin: 0; font-size: 20px; display: flex; align-items: center; gap: 10px;">
                                    📊 Tüm Zamanlar Ortalaması
                                </h3>
                                <p style="margin: 5px 0; font-size: 14px; opacity: 0.9;">
                                    ${currentUser.test_history.length} test ortalaması
                                </p>
                            </div>
                            <div style="text-align: right;">
                                <div style="font-size: 36px; font-weight: bold;">
                                    ${avgScore}%
                                </div>
                                <div style="font-size: 12px; opacity: 0.9;">Ortalama Skor</div>
                            </div>
                        </div>
                        
                        <div style="margin-top: 20px;">
                            <button class="btn" style="margin: 5px; background: white; color: #667eea;" onclick="viewAverageReport()">
                                📈 Ortalama Raporu Görüntüle
                            </button>
                            <button class="btn" style="margin: 5px; background: rgba(255,255,255,0.2);" onclick="viewProgressChart()">
                                📉 İlerleme Grafiği
                            </button>
                        </div>
                    </div>
                `;
            }
            
            // Test geçmişini tarih sırasına göre sırala (en yeni önce)
            const sortedHistory = [...currentUser.test_history].sort((a, b) => 
                new Date(b.test_date) - new Date(a.test_date)
            );

            sortedHistory.forEach((test, index) => {
                const testDate = new Date(test.test_date);
                const dateStr = testDate.toLocaleDateString('tr-TR', { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit'
                });

                html += `
                    <div style="background: white; border-radius: 15px; padding: 25px; box-shadow: 0 4px 15px rgba(0,0,0,0.1);">
                        <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 15px;">
                            <div>
                                <h3 style="margin: 0; color: #667eea; font-size: 18px;">
                                    ${index === 0 ? '🆕 ' : ''}Test #${sortedHistory.length - index}
                                </h3>
                                <p style="margin: 5px 0; color: #666; font-size: 14px;">📅 ${dateStr}</p>
                            </div>
                            <div style="text-align: right;">
                                <div style="font-size: 32px; font-weight: bold; color: #667eea;">
                                    ${test.overall_score}%
                                </div>
                                <div style="font-size: 12px; color: #999;">Genel Skor</div>
                            </div>
                        </div>
                        
                        <div style="margin-top: 20px;">
                            <button class="btn" style="margin: 5px;" onclick="viewHistoricalReport(${index})">
                                📊 Bu Raporu Görüntüle
                            </button>
                            <button class="btn" style="margin: 5px; background: #43e97b;" onclick="downloadHistoricalPDF(${index})">
                                📄 PDF İndir
                            </button>
                            ${index > 0 ? `
                                <button class="btn" style="margin: 5px; background: #f5576c;" onclick="compareReports(${index}, 0)">
                                    🔄 En Yeni ile Karşılaştır
                                </button>
                            ` : ''}
                        </div>
                    </div>
                `;
            });

            html += '</div>';
            container.innerHTML = html;
        }

        function viewHistoricalReport(index) {
            if (!currentUser || !currentUser.test_history) return;
            
            const sortedHistory = [...currentUser.test_history].sort((a, b) => 
                new Date(b.test_date) - new Date(a.test_date)
            );
            
            const test = sortedHistory[index];
            
            // Geçmiş rapor bilgisini kaydet
            window.isHistoricalReport = true;
            window.historicalReportDate = test.test_date;
            
            // Global değişkene test sonuçlarını yükle
            window.categoryScoresGlobal = JSON.parse(test.test_results);
            
            // Sonuç ekranını göster
            hideAllScreens();
            document.getElementById('resultsContainer').style.display = 'block';
            
            // Skorları göster
            document.getElementById('overallScore').textContent = test.overall_score + '%';
            
            // Geçmiş rapor uyarısı ekle
            const testDate = new Date(test.test_date);
            const dateStr = testDate.toLocaleDateString('tr-TR', { 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric',
                hour: '2-digit',
                minute: '2-digit'
            });
            
            // Başlığı güncelle
            const resultsTitle = document.querySelector('.results-title');
            if (resultsTitle) {
                resultsTitle.innerHTML = `
                    📜 Geçmiş Rapor - Test #${sortedHistory.length - index}
                    <div style="font-size: 14px; color: #666; font-weight: normal; margin-top: 5px;">
                        📅 ${dateStr}
                    </div>
                `;
            }
            
            // Yorum oluştur
            let interpretation = '';
            if (test.overall_score >= 85) {
                interpretation = 'Mükemmel! Kariyer gelişiminizde çok güçlü bir konumdasınız.';
            } else if (test.overall_score >= 70) {
                interpretation = 'Çok iyi! Güçlü yönleriniz var, bazı alanlarda gelişim fırsatları mevcut.';
            } else if (test.overall_score >= 60) {
                interpretation = 'İyi seviyede! Belirli alanlarda odaklanarak daha da güçlenebilirsiniz.';
            } else if (test.overall_score >= 45) {
                interpretation = 'Orta seviyede. Gelişim için net yol haritası belirlenebilir.';
            } else {
                interpretation = 'Gelişim potansiyeli yüksek! Sistematik çalışmayla büyük ilerleme kaydedebilirsiniz.';
            }
            document.getElementById('scoreInterpretation').textContent = interpretation;
            
            // Butonları geçmiş rapor için güncelle
            const resultsActions = document.getElementById('resultsActions');
            if (resultsActions) {
                resultsActions.innerHTML = `
                    <button class="btn" onclick="showDetailedReport()">Detaylı Raporu Görüntüle</button>
                    <button class="btn" onclick="downloadHistoricalPDF(${index})">📄 PDF Rapor İndir</button>
                    <button class="btn btn-secondary" onclick="showMyReports()">← Raporlara Dön</button>
                    <button class="btn btn-secondary" onclick="backToWelcome()">Ana Menüye Dön</button>
                `;
            }
            
            // Kategori sonuçlarını göster
            const categoryResultsContainer = document.getElementById('categoryResults');
            categoryResultsContainer.innerHTML = '';
            
            window.categoryScoresGlobal.forEach(category => {
                const categoryDiv = document.createElement('div');
                categoryDiv.className = 'category-result';
                
                categoryDiv.innerHTML = `
                    <div class="category-name">${category.name}</div>
                    <div class="category-score">
                        <span>${Math.round(category.percentage)}%</span>
                        <div class="score-bar">
                            <div class="score-fill" style="width: ${category.percentage}%"></div>
                        </div>
                        <span class="score-value">${category.score}/40</span>
                    </div>
                `;
                
                categoryResultsContainer.appendChild(categoryDiv);
            });
        }

        function downloadHistoricalPDF(index) {
            viewHistoricalReport(index);
            setTimeout(() => {
                downloadPDFReport();
            }, 500);
        }

        function viewAverageReport() {
            if (!currentUser || !currentUser.test_history || currentUser.test_history.length === 0) return;
            
            // Tüm testlerin ortalamasını hesapla
            const categoryAverages = {};
            
            // Her kategori için ortalama hesapla
            currentUser.test_history.forEach(test => {
                const results = JSON.parse(test.test_results);
                results.forEach(category => {
                    if (!categoryAverages[category.name]) {
                        categoryAverages[category.name] = {
                            name: category.name,
                            totalScore: 0,
                            totalPercentage: 0,
                            count: 0
                        };
                    }
                    categoryAverages[category.name].totalScore += category.score;
                    categoryAverages[category.name].totalPercentage += category.percentage;
                    categoryAverages[category.name].count++;
                });
            });
            
            // Ortalama skorları hesapla
            const avgCategoryScores = Object.values(categoryAverages).map(cat => ({
                name: cat.name,
                score: Math.round(cat.totalScore / cat.count),
                percentage: cat.totalPercentage / cat.count
            }));
            
            const avgOverallScore = Math.round(
                currentUser.test_history.reduce((sum, test) => sum + test.overall_score, 0) / 
                currentUser.test_history.length
            );
            
            // Global değişkene kaydet
            window.isHistoricalReport = true;
            window.isAverageReport = true;
            window.categoryScoresGlobal = avgCategoryScores;
            
            // Sonuç ekranını göster
            hideAllScreens();
            document.getElementById('resultsContainer').style.display = 'block';
            
            // Skorları göster
            document.getElementById('overallScore').textContent = avgOverallScore + '%';
            
            // Başlığı güncelle
            const resultsTitle = document.querySelector('.results-title');
            if (resultsTitle) {
                resultsTitle.innerHTML = `
                    📊 Tüm Zamanlar Ortalama Raporu
                    <div style="font-size: 14px; color: #666; font-weight: normal; margin-top: 5px;">
                        ${currentUser.test_history.length} test ortalaması
                    </div>
                `;
            }
            
            // Yorum
            let interpretation = `${currentUser.test_history.length} test ortalamanıza göre, `;
            if (avgOverallScore >= 85) {
                interpretation += 'kariyer gelişiminizde sürekli güçlü bir performans sergiliyorsunuz!';
            } else if (avgOverallScore >= 70) {
                interpretation += 'genel olarak iyi bir performans gösteriyorsunuz. Bazı alanlarda tutarlı gelişim fırsatları var.';
            } else if (avgOverallScore >= 60) {
                interpretation += 'dengeli bir gelişim gösteriyorsunuz. Belirli alanlarda odaklanarak daha da güçlenebilirsiniz.';
            } else if (avgOverallScore >= 45) {
                interpretation += 'orta seviyede bir performans gösteriyorsunuz. Gelişim için net yol haritası belirlenebilir.';
            } else {
                interpretation += 'sürekli gelişim potansiyeliniz yüksek. Sistematik çalışmayla büyük ilerleme kaydedebilirsiniz.';
            }
            document.getElementById('scoreInterpretation').textContent = interpretation;
            
            // Butonları güncelle
            const resultsActions = document.getElementById('resultsActions');
            if (resultsActions) {
                resultsActions.innerHTML = `
                    <button class="btn" onclick="showDetailedReport()">Detaylı Raporu Görüntüle</button>
                    <button class="btn" onclick="downloadAveragePDFReport()">📄 PDF Rapor İndir</button>
                    <button class="btn" onclick="viewProgressChart()">📉 İlerleme Grafiği</button>
                    <button class="btn btn-secondary" onclick="showMyReports()">← Raporlara Dön</button>
                    <button class="btn btn-secondary" onclick="backToWelcome()">Ana Menüye Dön</button>
                `;
            }
            
            // Kategori sonuçlarını göster
            const categoryResultsContainer = document.getElementById('categoryResults');
            categoryResultsContainer.innerHTML = '';
            
            avgCategoryScores.forEach(category => {
                const categoryDiv = document.createElement('div');
                categoryDiv.className = 'category-result';
                
                categoryDiv.innerHTML = `
                    <div class="category-name">${category.name}</div>
                    <div class="category-score">
                        <span>${Math.round(category.percentage)}%</span>
                        <div class="score-bar">
                            <div class="score-fill" style="width: ${category.percentage}%"></div>
                        </div>
                        <span class="score-value">${category.score}/40 (ort.)</span>
                    </div>
                `;
                
                categoryResultsContainer.appendChild(categoryDiv);
            });
        }

        function viewProgressChart() {
            if (!currentUser || !currentUser.test_history || currentUser.test_history.length === 0) return;
            
            hideAllScreens();
            
            // İlerleme grafik ekranı oluştur
            const container = document.createElement('div');
            container.id = 'progressChartScreen';
            container.className = 'results-container';
            container.style.display = 'block';
            
            const sortedHistory = [...currentUser.test_history].sort((a, b) => 
                new Date(a.test_date) - new Date(b.test_date)
            );
            
            let html = `
                <div class="results-header">
                    <h2 class="results-title">📉 Kariyer Gelişim İlerleme Grafiği</h2>
                    <p style="text-align: center; color: #666; margin-top: 10px;">
                        ${sortedHistory.length} test sonuçlarınızın zamana göre değişimi
                    </p>
                </div>
                
                <div style="background: white; border-radius: 15px; padding: 30px; margin: 20px 0;">
                    <h3 style="margin-bottom: 20px; color: #667eea;">📈 Genel Skor İlerlemesi</h3>
                    <div style="position: relative; height: 300px; border: 1px solid #e0e0e0; border-radius: 10px; padding: 20px; background: #f9f9f9;">
            `;
            
            // Basit çizgi grafiği (ASCII stil)
            const maxScore = 100;
            const chartHeight = 250;
            const chartWidth = sortedHistory.length * 100;
            
            sortedHistory.forEach((test, index) => {
                const testDate = new Date(test.test_date).toLocaleDateString('tr-TR', { month: 'short', day: 'numeric' });
                const percentage = test.overall_score;
                const barHeight = (percentage / maxScore) * chartHeight;
                const left = (index / (sortedHistory.length - 1)) * 80 + 10;
                
                html += `
                    <div style="position: absolute; bottom: 20px; left: ${left}%; transform: translateX(-50%);">
                        <div style="position: relative;">
                            <div style="
                                width: 60px;
                                height: ${barHeight}px;
                                background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
                                border-radius: 5px;
                                margin-bottom: 5px;
                                position: relative;
                                box-shadow: 0 2px 10px rgba(102, 126, 234, 0.3);
                            ">
                                <span style="
                                    position: absolute;
                                    top: -25px;
                                    left: 50%;
                                    transform: translateX(-50%);
                                    font-weight: bold;
                                    color: #667eea;
                                    font-size: 14px;
                                ">${percentage}%</span>
                            </div>
                            <div style="text-align: center; font-size: 11px; color: #666; white-space: nowrap;">
                                ${testDate}
                            </div>
                        </div>
                    </div>
                `;
            });
            
            html += `
                    </div>
                </div>
                
                <div style="background: white; border-radius: 15px; padding: 30px; margin: 20px 0;">
                    <h3 style="margin-bottom: 20px; color: #667eea;">📊 Test Detayları</h3>
                    <table style="width: 100%; border-collapse: collapse;">
                        <thead>
                            <tr style="background: #f5f5f5;">
                                <th style="padding: 12px; text-align: left; border-bottom: 2px solid #ddd;">Test #</th>
                                <th style="padding: 12px; text-align: left; border-bottom: 2px solid #ddd;">Tarih</th>
                                <th style="padding: 12px; text-align: center; border-bottom: 2px solid #ddd;">Skor</th>
                                <th style="padding: 12px; text-align: center; border-bottom: 2px solid #ddd;">Değişim</th>
                            </tr>
                        </thead>
                        <tbody>
            `;
            
            sortedHistory.forEach((test, index) => {
                const testDate = new Date(test.test_date).toLocaleDateString('tr-TR', { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit'
                });
                
                let change = '';
                if (index > 0) {
                    const diff = test.overall_score - sortedHistory[index - 1].overall_score;
                    if (diff > 0) {
                        change = `<span style="color: #4caf50;">↗️ +${diff}%</span>`;
                    } else if (diff < 0) {
                        change = `<span style="color: #f44336;">↘️ ${diff}%</span>`;
                    } else {
                        change = `<span style="color: #999;">➡️ 0%</span>`;
                    }
                }
                
                html += `
                    <tr style="border-bottom: 1px solid #eee;">
                        <td style="padding: 12px;">Test #${index + 1}</td>
                        <td style="padding: 12px;">${testDate}</td>
                        <td style="padding: 12px; text-align: center; font-weight: bold; color: #667eea;">${test.overall_score}%</td>
                        <td style="padding: 12px; text-align: center;">${change}</td>
                    </tr>
                `;
            });
            
            html += `
                        </tbody>
                    </table>
                </div>
                
                <div style="margin-top: 30px; text-align: center;">
                    <button class="btn" onclick="downloadProgressPDFReport()">📄 PDF Rapor İndir</button>
                    <button class="btn" onclick="showMyReports()">← Raporlara Dön</button>
                    <button class="btn btn-secondary" onclick="backToWelcome()">Ana Menüye Dön</button>
                </div>
            `;
            
            container.innerHTML = html;
            document.body.appendChild(container);
        }

        function compareReports(oldIndex, newIndex) {
            if (!currentUser || !currentUser.test_history) return;
            
            const sortedHistory = [...currentUser.test_history].sort((a, b) => 
                new Date(b.test_date) - new Date(a.test_date)
            );
            
            const oldTest = sortedHistory[oldIndex];
            const newTest = sortedHistory[newIndex];
            
            const oldResults = JSON.parse(oldTest.test_results);
            const newResults = JSON.parse(newTest.test_results);
            
            hideAllScreens();
            
            // Karşılaştırma ekranı oluştur
            const container = document.createElement('div');
            container.id = 'comparisonScreen';
            container.className = 'results-container';
            container.style.display = 'block';
            
            const oldDate = new Date(oldTest.test_date).toLocaleDateString('tr-TR');
            const newDate = new Date(newTest.test_date).toLocaleDateString('tr-TR');
            const scoreDiff = newTest.overall_score - oldTest.overall_score;
            
            let html = `
                <div class="results-header">
                    <h2 class="results-title">📊 Test Karşılaştırma</h2>
                    <p style="text-align: center; color: #666;">
                        <strong style="color: #f5576c;">${oldDate}</strong> 
                        🔄 
                        <strong style="color: #43e97b;">${newDate}</strong>
                    </p>
                </div>
                
                <div style="background: white; border-radius: 15px; padding: 25px; margin: 20px 0; box-shadow: 0 4px 15px rgba(0,0,0,0.1);">
                    <h3 style="text-align: center; margin-bottom: 20px; color: #667eea;">Genel Skor Değişimi</h3>
                    <div style="text-align: center; font-size: 28px; font-weight: bold; color: #333; padding: 20px;">
                        <span style="color: #f5576c;">${oldTest.overall_score}%</span>
                        <span style="color: #667eea; margin: 0 15px;">→</span>
                        <span style="color: #43e97b;">${newTest.overall_score}%</span>
                        <span style="color: ${scoreDiff >= 0 ? '#43e97b' : '#f5576c'}; margin-left: 15px;">
                            (${scoreDiff >= 0 ? '+' : ''}${scoreDiff}%)
                        </span>
                    </div>
                </div>
                
                <div class="category-results">
            `;
            
            // Kategori bazlı karşılaştırma
            oldResults.forEach((oldCat, index) => {
                const newCat = newResults[index];
                const change = newCat.percentage - oldCat.percentage;
                
                html += `
                    <div class="category-result" style="padding: 20px;">
                        <div class="category-name">${oldCat.name}</div>
                        <div style="display: flex; justify-content: space-between; align-items: center; margin-top: 10px;">
                            <div style="text-align: center; flex: 1;">
                                <div style="font-size: 11px; color: #999;">Eski</div>
                                <div style="font-size: 24px; font-weight: bold; color: #f5576c;">${Math.round(oldCat.percentage)}%</div>
                            </div>
                            <div style="flex: 1; text-align: center;">
                                <div style="font-size: 32px;">→</div>
                            </div>
                            <div style="text-align: center; flex: 1;">
                                <div style="font-size: 11px; color: #999;">Yeni</div>
                                <div style="font-size: 24px; font-weight: bold; color: #43e97b;">${Math.round(newCat.percentage)}%</div>
                            </div>
                            <div style="text-align: center; flex: 1;">
                                <div style="font-size: 11px; color: #999;">Fark</div>
                                <div style="font-size: 24px; font-weight: bold; color: ${change >= 0 ? '#43e97b' : '#f5576c'};">
                                    ${change >= 0 ? '+' : ''}${Math.round(change)}%
                                    ${change > 0 ? '📈' : change < 0 ? '📉' : '➡️'}
                                </div>
                            </div>
                        </div>
                    </div>
                `;
            });
            
            html += `
                </div>
                <div style="margin-top: 30px; text-align: center;">
                    <button class="btn" onclick="downloadComparisonPDFReport(${oldIndex}, ${newIndex})">📄 PDF Rapor İndir</button>
                    <button class="btn btn-secondary" onclick="closeComparison()">← Geri Dön</button>
                </div>
            `;
            
            container.innerHTML = html;
            
            // Eski karşılaştırma ekranını kaldır
            const oldComparison = document.getElementById('comparisonScreen');
            if (oldComparison) {
                oldComparison.remove();
            }
            
            document.querySelector('.container').appendChild(container);
        }

        function closeComparison() {
            const comparisonScreen = document.getElementById('comparisonScreen');
            if (comparisonScreen) {
                comparisonScreen.remove();
            }
            showMyReports();
        }

        function showDetailedReport() {
            // Dinamik olarak oluşturulmuş ekranları kaldır
            const progressChart = document.getElementById('progressChartScreen');
            if (progressChart) progressChart.remove();
            
            const comparison = document.getElementById('comparisonScreen');
            if (comparison) comparison.remove();
            
            // Sonuç ekranını göster
            document.getElementById('resultsContainer').style.display = 'block';
            
            // Detaylı rapor ekranını göster
            document.getElementById('resultsContainer').style.display = 'none';
            document.getElementById('reportContainer').style.display = 'block';
            
            // Genel skoru rapor ekranına aktar
            const overallScore = document.getElementById('overallScore').textContent;
            document.getElementById('reportOverallScore').textContent = overallScore;
            
            // Grafikleri çiz
            drawCharts();
            
            // Analizleri oluştur
            generateAnalyses();
        }

        function backToResults() {
            document.getElementById('reportContainer').style.display = 'none';
            document.getElementById('resultsContainer').style.display = 'block';
        }

        // Mesaj gösterme
        function showMessage(message, type) {
            // Basit toast mesajı
            const toast = document.createElement('div');
            let backgroundColor;
            
            switch(type) {
                case 'success':
                    backgroundColor = '#28a745';
                    break;
                case 'info':
                    backgroundColor = '#17a2b8';
                    break;
                case 'error':
                default:
                    backgroundColor = '#dc3545';
                    break;
            }
            
            toast.style.cssText = `
                position: fixed;
                top: 20px;
                left: 50%;
                transform: translateX(-50%);
                padding: 15px 20px;
                border-radius: 8px;
                color: white;
                font-weight: bold;
                z-index: 10000;
                max-width: 90%;
                width: auto;
                min-width: 250px;
                background: ${backgroundColor};
                box-shadow: 0 4px 12px rgba(0,0,0,0.2);
                text-align: center;
                animation: slideDown 0.3s ease-out;
            `;
            toast.textContent = message;
            document.body.appendChild(toast);
            
            setTimeout(() => {
                if (document.body.contains(toast)) {
                    toast.style.animation = 'slideUp 0.3s ease-in';
                    setTimeout(() => {
                        if (document.body.contains(toast)) {
                            document.body.removeChild(toast);
                        }
                    }, 300);
                }
            }, type === 'info' ? 3000 : 5000);
        }

        // Quiz verileri (D şıkları daha dengeli hale getirildi)
        const quizData = {
            categories: [
                {
                    name: "Stratejik Kariyer Planlaması",
                    questions: [
                        {
                            text: "Kariyer hedeflerinizi belirlerken hangi yaklaşımı benimsersiniz?",
                            options: [
                                { text: "Mevcut durumdan memnunum, özel bir hedef belirlemem", score: 1 },
                                { text: "Kısa vadeli hedefler belirler, duruma göre revize ederim", score: 2 },
                                { text: "Orta ve uzun vadeli hedeflerimi net olarak tanımlarım", score: 3 },
                                { text: "Kapsamlı kariyer planı yapar, düzenli olarak gözden geçiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer yol haritanızı oluştururken hangi faktörleri önceliklersiniz?",
                            options: [
                                { text: "Sadece maaş artışı ve pozisyon yükselmesini dikkate alırım", score: 1 },
                                { text: "İş güvenliği ve sosyal hakları öncelik veririm", score: 2 },
                                { text: "Kişisel gelişim fırsatları ve öğrenme imkanlarını değerlendiririm", score: 3 },
                                { text: "Sektör trendleri ve gelecek becerileri dahil çok boyutlu analiz yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer geçişleri konusunda nasıl bir strateji izlersiniz?",
                            options: [
                                { text: "Geçiş yapmaktan kaçınır, mevcut pozisyonumda kalmayı tercih ederim", score: 1 },
                                { text: "Zorunlu durumlar dışında geçiş yapmam", score: 2 },
                                { text: "Fırsatları değerlendirerek planlı geçişler yaparım", score: 3 },
                                { text: "Proaktif olarak yeni alanları keşfeder, esnek kariyer stratejileri geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Profesyonel gelişiminizi nasıl ölçümlersiniz?",
                            options: [
                                { text: "Herhangi bir ölçüm yapmam, sezgisel olarak değerlendiririm", score: 1 },
                                { text: "Yıllık performans değerlendirmelerini baz alırım", score: 2 },
                                { text: "Belirli KPI'lar ve hedefler üzerinden takip ederim", score: 3 },
                                { text: "Çok yönlü geri bildirim ve sürekli öz değerlendirme sistemi kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer riskleri karşısında nasıl bir yaklaşım sergilersiniz?",
                            options: [
                                { text: "Risk almaktan kaçınır, güvenli seçenekleri tercih ederim", score: 1 },
                                { text: "Sadece hesaplanmış riskler alırım", score: 2 },
                                { text: "Risk-fayda analizini yaparak bilinçli kararlar veririm", score: 3 },
                                { text: "Dengeli risk portföyü oluşturarak çeşitlendirilmiş strateji uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Sektörünüzdeki değişimleri kariyer planınıza nasıl entegre edersiniz?",
                            options: [
                                { text: "Değişimleri takip etmem, mevcut bilgilerimle devam ederim", score: 1 },
                                { text: "Büyük değişimleri fark ettiğimde tepki veririm", score: 2 },
                                { text: "Düzenli olarak sektör trendlerini takip eder, planımı güncellerim", score: 3 },
                                { text: "Gelecek öngörüleri yaparak değişimlere proaktif hazırlanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer mentorluğu ve koçluk konusunda nasıl bir tutum sergilersiniz?",
                            options: [
                                { text: "Mentor veya koç desteği almam, kendi başıma ilerlerim", score: 1 },
                                { text: "Sadece ihtiyaç duyduğumda danışmanlık alırım", score: 2 },
                                { text: "Düzenli mentor ilişkileri kurar, geri bildirim alırım", score: 3 },
                                { text: "Çok yönlü mentorluk ağı oluşturur, aynı zamanda başkalarına da mentor olurum", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer hedeflerinizi gerçekleştirmek için kaynak planlaması nasıl yaparsınız?",
                            options: [
                                { text: "Kaynak planlaması yapmam, duruma göre hareket ederim", score: 1 },
                                { text: "Temel ihtiyaçları karşılayacak kadar planlama yaparım", score: 2 },
                                { text: "Zaman, para ve enerji kaynaklarımı sistematik olarak planlırım", score: 3 },
                                { text: "Detaylı analiz yaparak optimal kaynak dağılımı stratejileri geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer başarınızı nasıl tanımlarsınız?",
                            options: [
                                { text: "Başarıyı net olarak tanımlamamışım", score: 1 },
                                { text: "Maddi kazanç ve pozisyon olarak görürüm", score: 2 },
                                { text: "İş-yaşam dengesi ve kişisel tatmin odaklı tanımlarım", score: 3 },
                                { text: "Çok boyutlu başarı kriterleri belirler, sürekli yeniden değerlendiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Kariyer planınızda esneklik ve adaptasyon nasıl yer alır?",
                            options: [
                                { text: "Sabit bir plan yapar, değiştirmem", score: 1 },
                                { text: "Büyük değişiklikler olduğunda planımı revize ederim", score: 2 },
                                { text: "Düzenli olarak planımı gözden geçirir, güncellerim", score: 3 },
                                { text: "Esnek kariyer yaklaşımı benimser, sürekli adaptasyon yaparım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Etkili İletişim ve Sunum",
                    questions: [
                        {
                            text: "Karmaşık konuları farklı hedef kitlelerine nasıl aktarırsınız?",
                            options: [
                                { text: "Herkese aynı şekilde, teknik detaylarla anlatırım", score: 1 },
                                { text: "Basitleştirmeye çalışır, genel ifadeler kullanırım", score: 2 },
                                { text: "Hedef kitleye göre dil ve örnekleri uyarlarım", score: 3 },
                                { text: "Hikaye anlatımı teknikleri kullanarak etkili iletişim kurarım", score: 4 }
                            ]
                        },
                        {
                            text: "Çatışmalı durumları nasıl yönetirsiniz?",
                            options: [
                                { text: "Çatışmadan kaçınır, konuyu ertelemeye çalışırım", score: 1 },
                                { text: "Kendi görüşümü savunur, karşı tarafı ikna etmeye çalışırım", score: 2 },
                                { text: "Aktif dinleme yaparak ortak çözüm ararım", score: 3 },
                                { text: "Çatışma dinamiklerini analiz ederek yapıcı çözümler üretirim", score: 4 }
                            ]
                        },
                        {
                            text: "Sunum yaparken hangi teknikleri kullanırsınız?",
                            options: [
                                { text: "Hazırladığım metni okur, slaytları takip ederim", score: 1 },
                                { text: "Ana noktaları vurgular, görsel destekler kullanırım", score: 2 },
                                { text: "İnteraktif öğeler ekler, dinleyici katılımını sağlarım", score: 3 },
                                { text: "Etkili sunum teknikleri uygular, çok duyulu deneyim yaratırım", score: 4 }
                            ]
                        },
                        {
                            text: "Geri bildirim verirken hangi yaklaşımı benimsersiniz?",
                            options: [
                                { text: "Doğrudan eleştiri yapar, neyin yanlış olduğunu söylerim", score: 1 },
                                { text: "Olumlu ve olumsuz noktaları dengeli şekilde aktarırım", score: 2 },
                                { text: "Yapıcı geri bildirim teknikleri kullanırım", score: 3 },
                                { text: "Gelişim odaklı yaklaşımla destekleyici diyalog kurarım", score: 4 }
                            ]
                        },
                        {
                            text: "Yazılı iletişimde hangi stratejileri uygularsınız?",
                            options: [
                                { text: "Düşündüklerimi doğrudan yazarım", score: 1 },
                                { text: "Açık ve anlaşılır olmaya dikkat ederim", score: 2 },
                                { text: "Yapılandırılmış format kullanır, önemli noktaları vurgularım", score: 3 },
                                { text: "Etkili yazım teknikleri uygular, okuyucu odaklı yaklaşım benimserim", score: 4 }
                            ]
                        },
                        {
                            text: "Dinleme becerilerinizi nasıl değerlendirirsiniz?",
                            options: [
                                { text: "Konuşurken cevabımı hazırlarım", score: 1 },
                                { text: "Dikkatli dinlemeye çalışır, ana mesajı anlarım", score: 2 },
                                { text: "Aktif dinleme teknikleri kullanır, doğrulama soruları sorarım", score: 3 },
                                { text: "Empatik dinleme yapar, söylenmeyenleri de algılarım", score: 4 }
                            ]
                        },
                        {
                            text: "Farklı kültürlerden insanlarla iletişim kurarken nasıl davranırsınız?",
                            options: [
                                { text: "Normal iletişim tarzımı sürdürürüm", score: 1 },
                                { text: "Daha dikkatli ve saygılı olmaya çalışırım", score: 2 },
                                { text: "Kültürel farklılıkları araştırır, uygun yaklaşım benimserim", score: 3 },
                                { text: "Kültürlerarası iletişim becerileri uygular, köprü kurucu rol oynarım", score: 4 }
                            ]
                        },
                        {
                            text: "Dijital iletişim araçlarını nasıl kullanırsınız?",
                            options: [
                                { text: "Temel özellikleri kullanır, standart mesajlar gönderirim", score: 1 },
                                { text: "Uygun platform seçimi yapar, mesajımı net iletmeye çalışırım", score: 2 },
                                { text: "Her platformun özelliklerini dikkate alır, içeriği optimize ederim", score: 3 },
                                { text: "Çok kanallı iletişim stratejisi uygular, dijital etki analizi yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "İkna etme becerilerinizi nasıl geliştirirsiniz?",
                            options: [
                                { text: "Doğal yeteneğime güvenir, özel çaba sarf etmem", score: 1 },
                                { text: "Güçlü argümanlar hazırlar, mantıklı yaklaşım benimserim", score: 2 },
                                { text: "Karşı tarafın motivasyonlarını anlar, ona göre strateji geliştiririm", score: 3 },
                                { text: "Etkili ikna prensipleri uygular, etik persuasion teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Topluluk önünde konuşma kaygınızı nasıl yönetirsiniz?",
                            options: [
                                { text: "Kaygı duyar, mümkün olduğunca kaçınırım", score: 1 },
                                { text: "Hazırlık yaparak kaygımı azaltmaya çalışırım", score: 2 },
                                { text: "Nefes teknikleri ve zihinsel hazırlık yaparım", score: 3 },
                                { text: "Kaygıyı enerjiye dönüştürür, performans teknikleri uygularım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Problem Çözme ve Kritik Düşünme",
                    questions: [
                        {
                            text: "Karmaşık problemlerle karşılaştığınızda ilk yaklaşımınız nedir?",
                            options: [
                                { text: "Hemen çözüm aramaya başlarım", score: 1 },
                                { text: "Problemi tanımlamaya çalışır, temel nedenleri ararım", score: 2 },
                                { text: "Sistematik analiz yapar, problemi parçalara ayırırım", score: 3 },
                                { text: "Kök neden analizi ve sistem düşüncesi uygular, çok boyutlu değerlendirme yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Karar verme sürecinizde hangi faktörleri dikkate alırsınız?",
                            options: [
                                { text: "Sezgilerime güvenir, hızlı karar veririm", score: 1 },
                                { text: "Temel artı-eksileri değerlendiririm", score: 2 },
                                { text: "Veri analizi yapar, alternatifleri karşılaştırırım", score: 3 },
                                { text: "Karar matrisi kullanır, senaryo analizi ve risk değerlendirmesi yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Yaratıcı çözümler geliştirmek için hangi yöntemleri kullanırsınız?",
                            options: [
                                { text: "Geleneksel yöntemleri tercih eder, denenmişi uygularım", score: 1 },
                                { text: "Farklı bakış açıları denemeye çalışırım", score: 2 },
                                { text: "Beyin fırtınası ve zihin haritası teknikleri kullanırım", score: 3 },
                                { text: "Tasarım düşüncesi ve yaratıcı problem çözme metodolojileri uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Belirsizlik durumlarında nasıl hareket edersiniz?",
                            options: [
                                { text: "Belirsizlikten rahatsız olur, kesin bilgi beklerim", score: 1 },
                                { text: "Mevcut bilgilerle en iyi tahmini yaparım", score: 2 },
                                { text: "Senaryo planlama yaparak alternatif stratejiler geliştiririm", score: 3 },
                                { text: "Çevik yaklaşım benimser, sürekli öğrenme ve adaptasyon stratejisi uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Analitik düşünme becerilerinizi nasıl kullanırsınız?",
                            options: [
                                { text: "Genel değerlendirmeler yapar, detaya inmem", score: 1 },
                                { text: "Önemli verileri inceler, temel analizler yaparım", score: 2 },
                                { text: "İstatistiksel analiz ve trend değerlendirmesi yaparım", score: 3 },
                                { text: "Veri analizi ve örüntü tanıma teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Farklı görüşleri değerlendirirken nasıl bir yaklaşım benimsersiniz?",
                            options: [
                                { text: "Kendi görüşümü doğru bulur, diğerlerini dikkate almam", score: 1 },
                                { text: "Farklı görüşleri dinler, kendi fikrimi korumaya çalışırım", score: 2 },
                                { text: "Objektif değerlendirme yapar, en mantıklı olanı seçerim", score: 3 },
                                { text: "Eleştirel değerlendirme yaklaşımı uygular, önyargıları minimize ederim", score: 4 }
                            ]
                        },
                        {
                            text: "Problem çözme sürecinizde işbirliğini nasıl kullanırsınız?",
                            options: [
                                { text: "Bireysel çalışmayı tercih eder, kendi başıma çözmeye çalışırım", score: 1 },
                                { text: "Gerektiğinde başkalarından yardım alırım", score: 2 },
                                { text: "Ekip çalışması yapar, farklı uzmanlıkları bir araya getiririm", score: 3 },
                                { text: "Kolektif zeka yaklaşımı benimser, işbirlikçi problem çözme teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Çözüm uygulaması sırasında nasıl bir strateji izlersiniz?",
                            options: [
                                { text: "Çözümü bulur, uygulamayı başkalarına bırakırım", score: 1 },
                                { text: "Temel adımları planlayarak uygulamaya başlarım", score: 2 },
                                { text: "Detaylı uygulama planı yapar, kilometre taşlarını takip ederim", score: 3 },
                                { text: "Değişim yönetimi prensipleri uygular, sürekli optimizasyon yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Başarısız çözümlerden nasıl öğrenirsiniz?",
                            options: [
                                { text: "Başarısızlığı unutmaya çalışır, geçmişte bırakırım", score: 1 },
                                { text: "Neyin yanlış gittiğini düşünür, bir daha yapmamaya çalışırım", score: 2 },
                                { text: "Sistematik analiz yapar, dersleri çıkarırım", score: 3 },
                                { text: "Hızlı başarısızlık yaklaşımı benimser, sürekli öğrenme döngüsü oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Etik ikilemlerle karşılaştığınızda nasıl karar verirsiniz?",
                            options: [
                                { text: "Kişisel çıkarlarımı önceleyerek karar veririm", score: 1 },
                                { text: "Genel kabul görmüş kurallara uyarım", score: 2 },
                                { text: "Paydaş analizi yaparak en az zarar verecek seçeneği bulurum", score: 3 },
                                { text: "Etik çerçeveler kullanarak çok boyutlu değerlendirme yaparım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Zaman ve Enerji Yönetimi",
                    questions: [
                        {
                            text: "Günlük önceliklerinizi nasıl belirlersiniz?",
                            options: [
                                { text: "Gelen işleri sırasıyla yaparım", score: 1 },
                                { text: "Acil olanları önce tamamlarım", score: 2 },
                                { text: "Önemli-acil analizi yaparak önceliklendiririm", score: 3 },
                                { text: "Değer odaklı önceliklendirme ve enerji yönetimi prensipleri uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Dikkat dağınıklığı ile nasıl başa çıkarsınız?",
                            options: [
                                { text: "Dikkatim dağıldığında o işi bırakır, başka işe geçerim", score: 1 },
                                { text: "Kendimi toplamaya çalışır, işe odaklanmaya çalışırım", score: 2 },
                                { text: "Zaman blokları ve odaklanma teknikleri kullanırım", score: 3 },
                                { text: "Derin çalışma prensipleri uygular, bilişsel yük yönetimi yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Çoklu görev konusunda nasıl bir yaklaşımınız var?",
                            options: [
                                { text: "Aynı anda birçok işi yapmaya çalışırım", score: 1 },
                                { text: "Önemli işlerde tek odak, rutin işlerde çoklu görev yaparım", score: 2 },
                                { text: "Görev değiştirme maliyetini dikkate alarak toplu işleme yaparım", score: 3 },
                                { text: "Dikkat kalıntısı teorisini uygular, tek görev optimizasyonu yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Enerji seviyenizi nasıl yönetirsiniz?",
                            options: [
                                { text: "Enerji yönetimi yapmam, sürekli aynı tempoda çalışırım", score: 1 },
                                { text: "Yorulduğumda mola verir, dinlenmeye çalışırım", score: 2 },
                                { text: "Günün farklı saatlerindeki enerji seviyemi takip ederim", score: 3 },
                                { text: "Biyolojik ritim optimizasyonu yaparak enerji döngülerini kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Delegasyon konusunda nasıl bir strateji izlersiniz?",
                            options: [
                                { text: "Her işi kendim yapmayı tercih ederim", score: 1 },
                                { text: "Sadece rutin işleri başkalarına veririm", score: 2 },
                                { text: "Kişilerin yeteneklerine göre görev dağılımı yaparım", score: 3 },
                                { text: "Güçlendirme yaklaşımı benimser, gelişim odaklı delegasyon yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Zaman planlaması yaparken hangi araçları kullanırsınız?",
                            options: [
                                { text: "Planlama yapmam, günü yaşarken karar veririm", score: 1 },
                                { text: "Basit yapılacaklar listesi tutarım", score: 2 },
                                { text: "Dijital takvim ve görev yönetimi uygulamaları kullanırım", score: 3 },
                                { text: "Kapsamlı zaman yönetimi sistemi ve zaman bloklaması metodolojisi uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Kesintilerle nasıl başa çıkarsınız?",
                            options: [
                                { text: "Her kesintiye anında cevap verir, işimi bırakırım", score: 1 },
                                { text: "Acil olanları halleder, diğerlerini ertelerim", score: 2 },
                                { text: "Kesinti yönetimi kuralları belirler, sınırlar koyarım", score: 3 },
                                { text: "Proaktif iletişim ve paydaş beklenti yönetimi yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Erteleme eğiliminizi nasıl yönetirsiniz?",
                            options: [
                                { text: "Erteleme eğilimim var, son dakikada yaparım", score: 1 },
                                { text: "Kendimi motive etmeye çalışır, zorla başlarım", score: 2 },
                                { text: "İşleri küçük parçalara böler, momentum yaratırım", score: 3 },
                                { text: "Erteleme psikolojisini anlayarak davranışsal müdahale teknikleri uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "İş-yaşam dengesini nasıl sağlarsınız?",
                            options: [
                                { text: "İş her zaman öncelikli, özel hayatım ikinci planda", score: 1 },
                                { text: "Mümkün olduğunca denge kurmaya çalışırım", score: 2 },
                                { text: "Net sınırlar belirler, her alana zaman ayırırım", score: 3 },
                                { text: "İş-yaşam entegrasyonu yaklaşımı benimser, bütüncül refah stratejisi uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Verimlilik ölçümünüzü nasıl yaparsınız?",
                            options: [
                                { text: "Verimlilik ölçümü yapmam, genel hissiyatla değerlendiririm", score: 1 },
                                { text: "Tamamladığım iş miktarına bakarım", score: 2 },
                                { text: "Hedef-gerçekleşme oranlarını takip ederim", score: 3 },
                                { text: "Sonuç odaklı verimlilik ölçümü sistemi kullanırım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Öz Liderlik ve Sorumluluk",
                    questions: [
                        {
                            text: "Kişisel gelişim hedeflerinizi nasıl belirlersiniz?",
                            options: [
                                { text: "Özel hedef belirlemem, doğal akışa bırakırım", score: 1 },
                                { text: "Genel hedefler belirler, duruma göre ilerlerim", score: 2 },
                                { text: "Akıllı hedefler koyar, düzenli takip ederim", score: 3 },
                                { text: "Çok yönlü değerlendirme yaparak kanıt temelli gelişim planlaması uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Hatalarınızla karşılaştığınızda nasıl tepki verirsiniz?",
                            options: [
                                { text: "Hataları gizlemeye çalışır, sorumluluğu başkasına atarım", score: 1 },
                                { text: "Hatamı kabul eder, özür dilerim", score: 2 },
                                { text: "Hatayı analiz eder, tekrarlanmaması için önlem alırım", score: 3 },
                                { text: "Büyüme zihniyeti yaklaşımı benimser, hatayı öğrenme fırsatına dönüştürürüm", score: 4 }
                            ]
                        },
                        {
                            text: "Öz disiplin konusunda nasıl bir yaklaşımınız var?",
                            options: [
                                { text: "Disiplin konusunda zorlanır, motivasyona bağlı kalırım", score: 1 },
                                { text: "Önemli konularda kendimi zorlar, disiplinli olmaya çalışırım", score: 2 },
                                { text: "Sistemli rutinler oluşturur, alışkanlık takibi yaparım", score: 3 },
                                { text: "Davranış psikolojisi prensipleri uygular, sürdürülebilir alışkanlık mimarisi oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Geri bildirim almaya nasıl yaklaşırsınız?",
                            options: [
                                { text: "Eleştiriyi kişisel saldırı olarak algılar, savunmaya geçerim", score: 1 },
                                { text: "Geri bildirimi dinler, mümkünse dikkate alırım", score: 2 },
                                { text: "Aktif olarak geri bildirim ister, yapıcı eleştirileri değerlendiririm", score: 3 },
                                { text: "Sürekli geri bildirim döngüsü oluşturur, çok yönlü geri bildirim sistemi kurarım", score: 4 }
                            ]
                        },
                        {
                            text: "Değerleriniz ve davranışlarınız arasındaki uyumu nasıl sağlarsınız?",
                            options: [
                                { text: "Değerlerimi net tanımlamamışım, duruma göre hareket ederim", score: 1 },
                                { text: "Temel değerlerim var, çoğunlukla uygun davranmaya çalışırım", score: 2 },
                                { text: "Değer sistemimi belirler, karar verirken referans alırım", score: 3 },
                                { text: "Değer temelli liderlik uygular, otantik liderlik prensipleri benimserim", score: 4 }
                            ]
                        },
                        {
                            text: "Kişisel marka oluşturma konusunda nasıl çalışırsınız?",
                            options: [
                                { text: "Kişisel marka konusunda düşünmem, doğal imajımla ilerlerim", score: 1 },
                                { text: "Profesyonel görünmeye dikkat eder, olumlu izlenim bırakmaya çalışırım", score: 2 },
                                { text: "Uzmanlık alanımı belirler, bu konuda tanınır olmaya çalışırım", score: 3 },
                                { text: "Kişisel marka stratejisi geliştir, düşünce liderliği pozisyonu oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Stresli durumlarda öz kontrolünüzü nasıl sağlarsınız?",
                            options: [
                                { text: "Stres altında kontrolümü kaybeder, tepkisel davranırım", score: 1 },
                                { text: "Sakinleşmeye çalışır, durumu kontrol etmeye çalışırım", score: 2 },
                                { text: "Nefes teknikleri ve farkındalık uygulamaları yaparım", score: 3 },
                                { text: "Duygusal düzenleme stratejileri uygular, dayanıklılık geliştirme teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Kişisel öğrenme stratejiniz nasıldır?",
                            options: [
                                { text: "Formal eğitim dışında özel öğrenme çabam yok", score: 1 },
                                { text: "İhtiyaç duyduğumda araştırma yapar, öğrenmeye çalışırım", score: 2 },
                                { text: "Düzenli okuma ve kurs alma alışkanlığım var", score: 3 },
                                { text: "Yaşam boyu öğrenme zihniyeti benimser, kişiselleştirilmiş öğrenme ekosistemi oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Hedeflerinize ulaşmada kararlılığınızı nasıl sürdürürsünüz?",
                            options: [
                                { text: "Zorluklar karşısında kolayca vazgeçer, hedeflerimi değiştiririm", score: 1 },
                                { text: "Motive olduğum zamanlarda ilerler, motivasyon düştüğünde duraklarım", score: 2 },
                                { text: "Sistematik plan yapar, kilometre taşlarına odaklanırım", score: 3 },
                                { text: "Azim ve sebat prensipleri uygular, engel-fırsat zihniyeti geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Etik karar verme süreciniz nasıldır?",
                            options: [
                                { text: "Kişisel çıkarlarımı önceleyerek karar veririm", score: 1 },
                                { text: "Genel ahlak kurallarına uygun davranmaya çalışırım", score: 2 },
                                { text: "Paydaş etkilerini değerlendirerek karar veririm", score: 3 },
                                { text: "Etik çerçeveler kullanarak ilkeli karar verme yaparım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Ekip Çalışması ve Çatışma Yönetimi",
                    questions: [
                        {
                            text: "Ekip içindeki rolünüzü nasıl tanımlarsınız?",
                            options: [
                                { text: "Sadece kendi işimi yapar, ekip dinamiklerine karışmam", score: 1 },
                                { text: "Verilen görevleri yerine getirir, gerektiğinde yardım ederim", score: 2 },
                                { text: "Proaktif olarak ekip başarısına katkı sağlarım", score: 3 },
                                { text: "Ekip dinamikleri uzmanı olarak, kolektif zekayı optimize ederim", score: 4 }
                            ]
                        },
                        {
                            text: "Ekip içi çatışmalara nasıl yaklaşırsınız?",
                            options: [
                                { text: "Çatışmadan kaçınır, taraf olmamaya çalışırım", score: 1 },
                                { text: "Kendi görüşümü savunur, haklı olduğumu kanıtlamaya çalışırım", score: 2 },
                                { text: "Arabulucu rolü oynar, ortak çözüm ararım", score: 3 },
                                { text: "Çatışma dönüşümü teknikleri uygular, çatışmayı büyüme fırsatına dönüştürürüm", score: 4 }
                            ]
                        },
                        {
                            text: "Farklı çalışma stillerine nasıl adapte olursunuz?",
                            options: [
                                { text: "Kendi stilimi sürdürür, başkalarının uyum sağlamasını beklerim", score: 1 },
                                { text: "Gerektiğinde esnek davranır, uyum sağlamaya çalışırım", score: 2 },
                                { text: "Ekip üyelerinin stillerini öğrenir, buna göre yaklaşım geliştiririm", score: 3 },
                                { text: "Kişilik araçları kullanarak davranışsal adaptasyon stratejileri uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Ekip kararlarına nasıl katkı sağlarsınız?",
                            options: [
                                { text: "Çoğunluğun kararına uyar, özel görüş belirtmem", score: 1 },
                                { text: "Fikrimi söyler, tartışmaya katılırım", score: 2 },
                                { text: "Veri ve analiz sunarak karar kalitesini artırmaya çalışırım", score: 3 },
                                { text: "Kolektif karar verme metodolojileri uygular, fikir birliği oluşturma teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Ekip performansını nasıl değerlendirirsiniz?",
                            options: [
                                { text: "Performans değerlendirmesi yapmam, genel hissiyatla yargılarım", score: 1 },
                                { text: "Sonuçlara bakarak başarı-başarısızlık değerlendirmesi yaparım", score: 2 },
                                { text: "Anahtar performans göstergeleri ve metrikler kullanarak objektif değerlendirme yaparım", score: 3 },
                                { text: "Ekip etkinliği çerçeveleri uygular, sürekli iyileştirme döngüsü oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Yeni ekip üyelerinin adaptasyonunu nasıl desteklersiniz?",
                            options: [
                                { text: "Yeni üyelerin kendi başlarına adapte olmasını beklerim", score: 1 },
                                { text: "Sorularını yanıtlar, temel bilgileri paylaşırım", score: 2 },
                                { text: "Mentorluk yapar, sistematik uyum desteği sağlarım", score: 3 },
                                { text: "Psikolojik güvenlik oluşturur, kapsayıcı uyum deneyimi tasarlarım", score: 4 }
                            ]
                        },
                        {
                            text: "Ekip içi iletişimi nasıl geliştirirsiniz?",
                            options: [
                                { text: "İletişim konusunda özel çaba sarf etmem", score: 1 },
                                { text: "Açık ve net iletişim kurmaya çalışırım", score: 2 },
                                { text: "Düzenli geri bildirim ve kontrol toplantıları yaparım", score: 3 },
                                { text: "İletişim sözleşmesi oluşturur, ekip iletişimi optimizasyonu yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Ekip motivasyonunu nasıl desteklersiniz?",
                            options: [
                                { text: "Motivasyon konusunda özel bir rolüm olduğunu düşünmem", score: 1 },
                                { text: "Pozitif olmaya çalışır, ekip moralini yüksek tutmaya çalışırım", score: 2 },
                                { text: "Başarıları kutlar, zorlu dönemlerde destek olurum", score: 3 },
                                { text: "İçsel motivasyon teorileri uygular, amaç odaklı katılım stratejileri geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Uzaktan çalışma ortamında ekip bağlılığını nasıl sürdürürsünüz?",
                            options: [
                                { text: "Uzaktan çalışmada ekip bağlılığı konusunda zorlanırım", score: 1 },
                                { text: "Düzenli toplantılar yapar, iletişimi sürdürmeye çalışırım", score: 2 },
                                { text: "Sanal ekip oluşturma aktiviteleri organize ederim", score: 3 },
                                { text: "Sanal işbirliği en iyi uygulamaları uygular, dijital ekip kültürü oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Ekip içi çeşitliliği nasıl değerlendirirsiniz?",
                            options: [
                                { text: "Çeşitlilik konusunda özel düşüncem yok, herkesi aynı şekilde görürüm", score: 1 },
                                { text: "Farklılıklara saygı duyar, herkesi eşit şekilde karşılarım", score: 2 },
                                { text: "Çeşitliliği güç olarak görür, farklı perspektifleri değerlendiririm", score: 3 },
                                { text: "Kapsayıcı liderlik prensipleri uygular, çeşitlilik ve kapsayıcılık savunucusu rolü oynarım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Öğrenme Çevikliği",
                    questions: [
                        {
                            text: "Yeni konuları öğrenirken hangi stratejileri kullanırsınız?",
                            options: [
                                { text: "Geleneksel yöntemlerle, kitap okuyarak öğrenirim", score: 1 },
                                { text: "Çeşitli kaynakları kullanır, not alarak öğrenirim", score: 2 },
                                { text: "Aktif öğrenme teknikleri uygular, pratik yaparak öğrenirim", score: 3 },
                                { text: "Üst bilişsel stratejiler kullanır, kişiselleştirilmiş öğrenme sistemi oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Başarısızlıklardan nasıl öğrenirsiniz?",
                            options: [
                                { text: "Başarısızlığı unutmaya çalışır, üzerinde durmam", score: 1 },
                                { text: "Neyin yanlış gittiğini düşünür, bir daha yapmamaya çalışırım", score: 2 },
                                { text: "Sistematik analiz yapar, dersleri çıkarırım", score: 3 },
                                { text: "Eylem sonrası değerlendirme metodolojisi uygular, başarısızlık-öğrenme dönüşümü yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Değişen koşullara nasıl adapte olursunuz?",
                            options: [
                                { text: "Değişime direnç gösterir, eski yöntemleri sürdürmeye çalışırım", score: 1 },
                                { text: "Zorunlu kaldığımda değişime uyum sağlarım", score: 2 },
                                { text: "Değişimi fırsat olarak görür, proaktif adaptasyon yaparım", score: 3 },
                                { text: "Değişim çevikliği prensipleri benimser, sürekli adaptasyon zihniyeti geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Farklı perspektifleri nasıl değerlendirirsiniz?",
                            options: [
                                { text: "Kendi bakış açımı doğru bulur, diğerlerini dikkate almam", score: 1 },
                                { text: "Farklı görüşleri dinler, kendi fikrimi korumaya çalışırım", score: 2 },
                                { text: "Açık fikirli yaklaşım sergiler, farklı perspektifleri değerlendiririm", score: 3 },
                                { text: "Perspektif alma yeteneği geliştir, bilişsel esnekliği maksimize ederim", score: 4 }
                            ]
                        },
                        {
                            text: "Belirsizlik durumlarında nasıl öğrenirsiniz?",
                            options: [
                                { text: "Belirsizlikten rahatsız olur, kesin bilgi beklerim", score: 1 },
                                { text: "Mevcut bilgilerle hareket eder, zamanla öğrenirim", score: 2 },
                                { text: "Deneme-yanılma yöntemiyle öğrenmeye çalışırım", score: 3 },
                                { text: "Belirsizlik toleransı geliştir, deneysel öğrenme yaklaşımı benimserim", score: 4 }
                            ]
                        },
                        {
                            text: "Geri bildirimden nasıl yararlanırsınız?",
                            options: [
                                { text: "Geri bildirimi kişisel eleştiri olarak algılar, savunmaya geçerim", score: 1 },
                                { text: "Yapıcı eleştirileri dinler, dikkate almaya çalışırım", score: 2 },
                                { text: "Aktif olarak geri bildirim ister, öğrenme fırsatı olarak görürüm", score: 3 },
                                { text: "Çok yönlü geri bildirim sistemi oluşturur, sürekli öğrenme döngüsü yaratırım", score: 4 }
                            ]
                        },
                        {
                            text: "Yeni teknolojileri nasıl öğrenirsiniz?",
                            options: [
                                { text: "Teknoloji öğrenmekten kaçınır, mevcut bilgilerimle yetinirim", score: 1 },
                                { text: "Zorunlu kaldığımda temel seviyede öğrenirim", score: 2 },
                                { text: "Proaktif olarak yeni teknolojileri takip eder, öğrenirim", score: 3 },
                                { text: "Dijital akıcılık geliştir, gelişmekte olan teknoloji benimseme stratejisi uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Öğrenme hızınızı nasıl artırırsınız?",
                            options: [
                                { text: "Doğal öğrenme hızımla yetinir, özel teknik kullanmam", score: 1 },
                                { text: "Daha fazla zaman ayırarak öğrenme hızımı artırmaya çalışırım", score: 2 },
                                { text: "Etkili öğrenme teknikleri araştırır, uygularım", score: 3 },
                                { text: "Hızlandırılmış öğrenme metodolojileri uygular, bilişsel geliştirme teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Karmaşık konuları nasıl öğrenirsiniz?",
                            options: [
                                { text: "Karmaşık konulardan kaçınır, basit olanları tercih ederim", score: 1 },
                                { text: "Adım adım öğrenmeye çalışır, sabırlı olurum", score: 2 },
                                { text: "Konuyu parçalara böler, sistematik yaklaşım benimserim", score: 3 },
                                { text: "Parçalama ve iskele kurma teknikleri kullanır, karmaşıklık yönetimi yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Öğrendiklerinizi nasıl uygularsınız?",
                            options: [
                                { text: "Teorik bilgiyi öğrenir, uygulamaya geçmekte zorlanırım", score: 1 },
                                { text: "Fırsat buldukça öğrendiklerimi uygulamaya çalışırım", score: 2 },
                                { text: "Sistematik olarak uygulama planı yapar, pratik yaparım", score: 3 },
                                { text: "Öğrenme transferi prensipleri uygular, bilgi-eylem köprüsü oluştururum", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Duygusal Zeka ve Stres Toleransı",
                    questions: [
                        {
                            text: "Kendi duygularınızı nasıl tanırsınız?",
                            options: [
                                { text: "Duygularımı fark etmem, tepkisel davranırım", score: 1 },
                                { text: "Güçlü duygular yaşadığımda fark ederim", score: 2 },
                                { text: "Duygularımı tanır, nedenlerini anlamaya çalışırım", score: 3 },
                                { text: "Duygusal ayrıntı geliştir, üst duygusal farkındalık uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Stresli durumlarla nasıl başa çıkarsınız?",
                            options: [
                                { text: "Stres altında kontrolümü kaybeder, panik yaparım", score: 1 },
                                { text: "Stresli durumları atlatmaya çalışır, dayanırım", score: 2 },
                                { text: "Stres yönetimi teknikleri kullanır, sakin kalmaya çalışırım", score: 3 },
                                { text: "Dayanıklılık geliştirme stratejileri uygular, stres-güç dönüşümü yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Başkalarının duygularını nasıl algılarsınız?",
                            options: [
                                { text: "Başkalarının duygularını fark etmem, kendi işime odaklanırım", score: 1 },
                                { text: "Açık duygusal ifadeleri fark eder, tepki veririm", score: 2 },
                                { text: "Sözsüz iletişimi okur, empati kurmaya çalışırım", score: 3 },
                                { text: "Duygusal bulaşma dinamiklerini anlayarak, ileri empati becerileri uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Çatışmalı durumlarda duygusal kontrolünüzü nasıl sağlarsınız?",
                            options: [
                                { text: "Çatışmada duygusal olur, kontrolümü kaybederim", score: 1 },
                                { text: "Sakin kalmaya çalışır, tepkimi kontrol etmeye çalışırım", score: 2 },
                                { text: "Nefes teknikleri kullanır, objektif kalmaya çalışırım", score: 3 },
                                { text: "Duygusal düzenleme stratejileri uygular, çatışma azaltma teknikleri kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Motivasyonunuzu nasıl sürdürürsünüz?",
                            options: [
                                { text: "Motivasyonum dış faktörlere bağlı, dalgalanma yaşarım", score: 1 },
                                { text: "Kendimi motive etmeye çalışır, pozitif düşünmeye çalışırım", score: 2 },
                                { text: "İçsel motivasyon kaynaklarımı belirler, bunlara odaklanırım", score: 3 },
                                { text: "Öz belirleme teorisi uygular, içsel motivasyon optimizasyonu yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Olumsuz duygularla nasıl başa çıkarsınız?",
                            options: [
                                { text: "Olumsuz duyguları bastırır, yok saymaya çalışırım", score: 1 },
                                { text: "Olumsuz duygulardan kaçınır, dikkatimi başka yöne çeviririm", score: 2 },
                                { text: "Olumsuz duyguları kabul eder, sağlıklı yollarla ifade ederim", score: 3 },
                                { text: "Bilişsel yeniden çerçeveleme teknikleri uygular, duygusal simya yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Sosyal ilişkilerde duygusal zekanızı nasıl kullanırsınız?",
                            options: [
                                { text: "Sosyal ilişkilerde duygusal boyutu dikkate almam", score: 1 },
                                { text: "İnsanlarla iyi geçinmeye çalışır, uyumlu olmaya çalışırım", score: 2 },
                                { text: "Karşımdakinin duygusal durumunu dikkate alarak yaklaşırım", score: 3 },
                                { text: "Sosyal duygusal zeka uygular, ilişki optimizasyonu yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Baskı altında karar verirken nasıl davranırsınız?",
                            options: [
                                { text: "Baskı altında panik yapar, yanlış kararlar veririm", score: 1 },
                                { text: "Stresli olsam da karar vermeye çalışır, elimden geleni yaparım", score: 2 },
                                { text: "Sakin kalmaya çalışır, mümkün olduğunca objektif değerlendirme yaparım", score: 3 },
                                { text: "Baskıya dayanıklı karar verme teknikleri uygular, baskı altında zarafet sergilerim", score: 4 }
                            ]
                        },
                        {
                            text: "Duygusal iyileşme sürecinizi nasıl yönetirsiniz?",
                            options: [
                                { text: "Duygusal yaralarım uzun süre iyileşmez, etkisinde kalırım", score: 1 },
                                { text: "Zamanla iyileşir, unutmaya çalışırım", score: 2 },
                                { text: "Aktif olarak iyileşme sürecini destekler, yardım alırım", score: 3 },
                                { text: "Travma sonrası büyüme prensipleri uygular, zorluk sonrası gelişim stratejileri geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Empati kurma becerinizi nasıl değerlendirirsiniz?",
                            options: [
                                { text: "Empati kurmakta zorlanır, kendi perspektifimde kalırım", score: 1 },
                                { text: "İnsanları anlamaya çalışır, onların yerine kendimi koymaya çalışırım", score: 2 },
                                { text: "Aktif dinleme yaparak empati kurar, duygusal destek sağlarım", score: 3 },
                                { text: "Bilişsel ve duygusal empati dengesi kurar, şefkatli liderlik uygularım", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Profesyonel Marka ve Ağ Yönetimi",
                    questions: [
                        {
                            text: "Kişisel markanızı nasıl tanımlarsınız?",
                            options: [
                                { text: "Kişisel marka konusunda düşünmem, doğal imajımla ilerlerim", score: 1 },
                                { text: "Profesyonel görünmeye dikkat eder, olumlu izlenim bırakmaya çalışırım", score: 2 },
                                { text: "Uzmanlık alanımı belirler, bu konuda tanınır olmaya çalışırım", score: 3 },
                                { text: "Stratejik kişisel marka yapar, otantik değer önerisi oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Profesyonel ağınızı nasıl geliştirirsiniz?",
                            options: [
                                { text: "Ağ oluşturma yapmam, mevcut çevremle yetinirim", score: 1 },
                                { text: "Etkinliklere katılır, yeni insanlarla tanışmaya çalışırım", score: 2 },
                                { text: "Sistematik ağ oluşturma yapar, ilişkileri sürdürmeye çalışırım", score: 3 },
                                { text: "Stratejik ilişki kurma uygular, karşılıklı değer yaratma odaklı ağ oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Sosyal medyada profesyonel varlığınızı nasıl yönetirsiniz?",
                            options: [
                                { text: "Sosyal medyayı profesyonel amaçla kullanmam", score: 1 },
                                { text: "Temel profil bilgilerimi güncel tutar, ara sıra paylaşım yaparım", score: 2 },
                                { text: "Düzenli içerik paylaşır, sektörümle ilgili konularda aktif olurum", score: 3 },
                                { text: "Dijital düşünce liderliği stratejisi uygular, içerik pazarlama ile uzmanlık sergilerim", score: 4 }
                            ]
                        },
                        {
                            text: "Mentorluk ilişkilerini nasıl yönetirsiniz?",
                            options: [
                                { text: "Mentor veya mentee olmam, kendi başıma ilerlerim", score: 1 },
                                { text: "İhtiyaç duyduğumda danışmanlık alır, bazen başkalarına yardım ederim", score: 2 },
                                { text: "Aktif mentor ilişkileri kurar, aynı zamanda başkalarına mentor olurum", score: 3 },
                                { text: "Mentorluk ekosistemi oluşturur, karşılıklı mentorluk ve akran mentorluğu uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Sektörünüzdeki görünürlüğünüzü nasıl artırırsınız?",
                            options: [
                                { text: "Görünürlük konusunda özel çaba sarf etmem", score: 1 },
                                { text: "İyi iş çıkararak doğal olarak tanınmaya çalışırım", score: 2 },
                                { text: "Konferanslara katılır, sunum yapar, makale yazarım", score: 3 },
                                { text: "Düşünce liderliği stratejisi geliştir, sektör etkisi oluşturma yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Profesyonel itibarınızı nasıl korursunuz?",
                            options: [
                                { text: "İtibar yönetimi konusunda özel düşüncem yok", score: 1 },
                                { text: "Etik davranmaya dikkat eder, sözümü tutmaya çalışırım", score: 2 },
                                { text: "Tutarlı davranış sergiler, güvenilir olmaya odaklanırım", score: 3 },
                                { text: "İtibar yönetimi stratejileri uygular, paydaş algı optimizasyonu yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "İş fırsatlarını nasıl yaratırsınız?",
                            options: [
                                { text: "Fırsatların kendiliğinden gelmesini beklerim", score: 1 },
                                { text: "Aktif olarak iş ararım, başvurular yaparım", score: 2 },
                                { text: "Ağımı kullanır, referanslar alırım", score: 3 },
                                { text: "Fırsat yaratma zihniyeti benimser, değer öncelikli yaklaşım uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Profesyonel gelişim hikayenizi nasıl anlatırsınız?",
                            options: [
                                { text: "Hikaye anlatımı yapmam, özgeçmişimdeki bilgileri aktarırım", score: 1 },
                                { text: "Temel deneyimlerimi kronolojik olarak anlatırım", score: 2 },
                                { text: "Başarılarımı ve öğrendiklerimi vurgulayarak anlatırım", score: 3 },
                                { text: "Etkileyici anlatı oluşturur, kahraman yolculuğu çerçevesi uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Sektör etkinliklerindeki rolünüz nasıldır?",
                            options: [
                                { text: "Etkinliklere katılmam, gerekli görmem", score: 1 },
                                { text: "Önemli etkinliklere katılır, dinleyici olarak yer alırım", score: 2 },
                                { text: "Aktif katılım gösterir, soru sorar, ağ oluşturma yaparım", score: 3 },
                                { text: "Etkinlik liderliği rolü oynar, topluluk oluşturma ve ekosistem geliştirme yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "Profesyonel referanslarınızı nasıl yönetirsiniz?",
                            options: [
                                { text: "Referans yönetimi yapmam, gerektiğinde isimleri veririm", score: 1 },
                                { text: "Güvendiğim kişilerin isimlerini referans olarak kullanırım", score: 2 },
                                { text: "Referanslarımla düzenli iletişim kurar, güncel tutarım", score: 3 },
                                { text: "Stratejik referans yönetimi yapar, karşılıklı savunuculuk ağı oluştururum", score: 4 }
                            ]
                        }
                    ]
                },
                {
                    name: "Yenilikçilik ve Geliştirme Odaklılık",
                    questions: [
                        {
                            text: "Yeni fikirler geliştirirken hangi yaklaşımı benimsersiniz?",
                            options: [
                                { text: "Geleneksel yöntemleri tercih eder, denenmişi uygularım", score: 1 },
                                { text: "Mevcut çözümleri geliştirmeye çalışırım", score: 2 },
                                { text: "Yaratıcı düşünme teknikleri kullanır, farklı yaklaşımlar denerim", score: 3 },
                                { text: "Tasarım düşüncesi metodolojisi uygular, yıkıcı inovasyon stratejileri geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Değişim önerilerinizi nasıl geliştirirsiniz?",
                            options: [
                                { text: "Değişim önerisi geliştirmem, mevcut durumu kabul ederim", score: 1 },
                                { text: "Gözlemlediğim sorunlar için basit çözümler önerrim", score: 2 },
                                { text: "Sistematik analiz yaparak iyileştirme önerileri geliştiririm", score: 3 },
                                { text: "Değişim yönetimi çerçeveleri kullanır, dönüşüm yol haritası oluştururum", score: 4 }
                            ]
                        },
                        {
                            text: "Teknolojik yenilikleri nasıl takip edersiniz?",
                            options: [
                                { text: "Teknolojik yenilikleri takip etmem, mevcut araçlarla yetinirim", score: 1 },
                                { text: "Popüler olan teknolojileri öğrenmeye çalışırım", score: 2 },
                                { text: "Sektörümle ilgili teknolojik gelişmeleri düzenli takip ederim", score: 3 },
                                { text: "Gelişmekte olan teknoloji keşfi yapar, erken benimseme stratejileri geliştiririm", score: 4 }
                            ]
                        },
                        {
                            text: "Süreç iyileştirme konusunda nasıl yaklaşırsınız?",
                            options: [
                                { text: "Mevcut süreçleri olduğu gibi takip ederim", score: 1 },
                                { text: "Sorun yaşadığımda o anki çözümler ararım", score: 2 },
                                { text: "Düzenli olarak süreçleri gözden geçirir, iyileştirme fırsatları ararım", score: 3 },
                                { text: "Sürekli iyileştirme kültürü oluşturur, yalın metodoloji ve kaizen uygularım", score: 4 }
                            ]
                        },
                        {
                            text: "Yaratıcılığınızı nasıl geliştirirsiniz?",
                            options: [
                                { text: "Yaratıcılık konusunda özel çaba sarf etmem", score: 1 },
                                { text: "Farklı kaynaklardan ilham almaya çalışırım", score: 2 },
                                { text: "Yaratıcılık egzersizleri yapar, farklı aktiviteler denerim", score: 3 },
                                { text: "Yaratıcı düşünme çerçeveleri kullanır, inovasyon laboratuvarı yaklaşımı benimserim", score: 4 }
                            ]
                        },
                        {
                            text: "Risk alma konusunda nasıl bir tutumunuz var?",
                            options: [
                                { text: "Risk almaktan kaçınır, güvenli seçenekleri tercih ederim", score: 1 },
                                { text: "Sadece hesaplanmış riskler alırım", score: 2 },
                                { text: "İnovasyon için gerekli riskleri almaya hazırım", score: 3 },
                                { text: "Akıllı risk alma stratejileri uygular, portföy yaklaşımı benimserim", score: 4 }
                            ]
                        },
                        {
                            text: "Başarısız denemelere nasıl yaklaşırsınız?",
                            options: [
                                { text: "Başarısızlıktan kaçınır, deneme yapmaktan çekinirim", score: 1 },
                                { text: "Başarısızlığı kötü bir deneyim olarak görürüm", score: 2 },
                                { text: "Başarısızlığı öğrenme fırsatı olarak değerlendiririm", score: 3 },
                                { text: "Hızlı başarısızlık metodolojisi uygular, hızlı prototipleme ve tekrarlı öğrenme yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "İnovasyon projelerini nasıl yönetirsiniz?",
                            options: [
                                { text: "İnovasyon projesi yönetimi konusunda deneyimim yok", score: 1 },
                                { text: "Temel proje yönetimi teknikleri kullanırım", score: 2 },
                                { text: "Çevik metodoloji uygular, tekrarlı geliştirme yaparım", score: 3 },
                                { text: "İnovasyon hattı yönetimi uygular, aşama-kapı süreci kullanırım", score: 4 }
                            ]
                        },
                        {
                            text: "Gelecek trendlerini nasıl değerlendirirsiniz?",
                            options: [
                                { text: "Gelecek trendleri konusunda düşünmem, bugüne odaklanırım", score: 1 },
                                { text: "Genel trendleri takip eder, haberlerden öğrenmeye çalışırım", score: 2 },
                                { text: "Sektörümle ilgili trend analizleri yapar, gelecek planlaması yaparım", score: 3 },
                                { text: "Gelecek öngörü metodolojileri uygular, senaryo planlama ve zayıf sinyal tespiti yaparım", score: 4 }
                            ]
                        },
                        {
                            text: "İnovatif çözümlerinizi nasıl hayata geçirirsiniz?",
                            options: [
                                { text: "Fikirlerim genelde teoride kalır, uygulamaya geçirmekte zorlanırım", score: 1 },
                                { text: "Basit fikirlerimi uygulamaya çalışırım", score: 2 },
                                { text: "Sistematik uygulama planı yaparak fikirlerimi hayata geçiririm", score: 3 },
                                { text: "İnovasyon-pazara hattı oluşturur, ticarileştirme stratejisi geliştiririm", score: 4 }
                            ]
                        }
                    ]
                }
            ]
        };

        // Quiz fonksiyonları
        function startQuiz() {
            if (!currentUser) {
                showMessage("Lütfen önce giriş yapın!", "error");
                return;
            }
            
            // Tüm ekranları gizle
            hideAllScreens();
            
            // Test ekranını aç
            document.getElementById('quizContainer').style.display = 'block';
            showQuestion();
        }

        function showQuestion() {
            const category = quizData.categories[currentCategoryIndex];
            const question = category.questions[currentQuestionInCategory];
            
            // Progress güncelleme
            const progress = ((currentQuestionIndex) / 100) * 100;
            document.getElementById('progressFill').style.width = progress + '%';
            
            // Soru bilgileri güncelleme
            document.getElementById('questionCounter').textContent = `Soru ${currentQuestionIndex + 1} / 100`;
            document.getElementById('categoryBadge').textContent = category.name;
            document.getElementById('questionText').textContent = question.text;
            
            // Seçenekleri oluşturma
            const optionsContainer = document.getElementById('optionsContainer');
            optionsContainer.innerHTML = '';
            
            question.options.forEach((option, index) => {
                const optionDiv = document.createElement('div');
                optionDiv.className = 'option';
                optionDiv.onclick = () => selectOption(index);
                
                optionDiv.innerHTML = `
                    <div class="option-label">${String.fromCharCode(65 + index)}</div>
                    <div class="option-text">${option.text}</div>
                `;
                
                optionsContainer.appendChild(optionDiv);
            });
            
            // Navigasyon butonları güncelleme
            document.getElementById('prevBtn').style.display = currentQuestionIndex === 0 ? 'none' : 'block';
            document.getElementById('nextBtn').disabled = true;
            
            // Önceki cevabı gösterme
            if (answers[currentQuestionIndex] !== undefined) {
                selectOption(answers[currentQuestionIndex], false);
            }
        }

        function selectOption(optionIndex, updateAnswer = true) {
            // Önceki seçimi temizle
            document.querySelectorAll('.option').forEach(opt => opt.classList.remove('selected'));
            
            // Yeni seçimi işaretle
            document.querySelectorAll('.option')[optionIndex].classList.add('selected');
            
            // Cevabı kaydet
            if (updateAnswer) {
                answers[currentQuestionIndex] = optionIndex;
            }
            
            // Sonraki butonunu aktif et
            document.getElementById('nextBtn').disabled = false;
        }

        function nextQuestion() {
            if (answers[currentQuestionIndex] === undefined) return;
            
            currentQuestionIndex++;
            currentQuestionInCategory++;
            
            // Kategori değişimi kontrolü
            if (currentQuestionInCategory >= 10) {
                currentCategoryIndex++;
                currentQuestionInCategory = 0;
            }
            
            if (currentQuestionIndex >= 100) {
                showResults();
            } else {
                showQuestion();
            }
        }

        function previousQuestion() {
            if (currentQuestionIndex === 0) return;
            
            currentQuestionIndex--;
            currentQuestionInCategory--;
            
            // Kategori değişimi kontrolü (geriye)
            if (currentQuestionInCategory < 0) {
                currentCategoryIndex--;
                currentQuestionInCategory = 9;
            }
            
            showQuestion();
        }

        async function showResults() {
            document.getElementById('quizContainer').style.display = 'none';
            document.getElementById('resultsContainer').style.display = 'block';
            
            // Yeni test bayrağını temizle
            window.isHistoricalReport = false;
            window.historicalReportDate = null;
            
            // Başlığı normal haline döndür
            const resultsTitle = document.querySelector('.results-title');
            if (resultsTitle) {
                resultsTitle.innerHTML = 'Kariyer Gelişim Raporu';
            }
            
            // Butonları normale döndür
            const resultsActions = document.getElementById('resultsActions');
            if (resultsActions) {
                resultsActions.innerHTML = `
                    <button class="btn" onclick="showDetailedReport()">Detaylı Raporu Görüntüle</button> 
                    <button class="btn" onclick="downloadPDFReport()">📄 PDF Rapor İndir</button> 
                    <button class="btn btn-secondary" onclick="backToWelcome()">Ana Menüye Dön</button>
                `;
            }
            
            // Kategori skorlarını hesapla
            const categoryScores = [];
            let totalScore = 0;
            
            quizData.categories.forEach((category, categoryIndex) => {
                let categoryScore = 0;
                const startIndex = categoryIndex * 10;
                
                for (let i = 0; i < 10; i++) {
                    const questionIndex = startIndex + i;
                    const answerIndex = answers[questionIndex];
                    const score = category.questions[i].options[answerIndex].score;
                    categoryScore += score;
                }
                
                categoryScores.push({
                    name: category.name,
                    score: categoryScore,
                    percentage: (categoryScore / 40) * 100
                });
                
                totalScore += categoryScore;
            });
            
            // Genel skor gösterimi
            const overallPercentage = (totalScore / 400) * 100;
            document.getElementById('overallScore').textContent = Math.round(overallPercentage) + '%';
            
            // Skor yorumu
            let interpretation = '';
            if (overallPercentage >= 85) {
                interpretation = 'Mükemmel! Kariyer gelişiminizde çok güçlü bir konumdasınız.';
            } else if (overallPercentage >= 70) {
                interpretation = 'Çok iyi! Güçlü yönleriniz var, bazı alanlarda gelişim fırsatları mevcut.';
            } else if (overallPercentage >= 60) {
                interpretation = 'İyi seviyede! Belirli alanlarda odaklanarak daha da güçlenebilirsiniz.';
            } else if (overallPercentage >= 45) {
                interpretation = 'Orta seviyede. Gelişim için net yol haritası belirlenebilir.';
            } else {
                interpretation = 'Gelişim potansiyeli yüksek! Sistematik çalışmayla büyük ilerleme kaydedebilirsiniz.';
            }
            
            document.getElementById('scoreInterpretation').textContent = interpretation;
            
            // Kategori sonuçlarını global değişkene kaydet
            window.categoryScoresGlobal = categoryScores;
            
            // Kategori sonuçlarını göster
            const categoryResultsContainer = document.getElementById('categoryResults');
            categoryResultsContainer.innerHTML = '';
            
            categoryScores.forEach(category => {
                const categoryDiv = document.createElement('div');
                categoryDiv.className = 'category-result';
                
                categoryDiv.innerHTML = `
                    <div class="category-name">${category.name}</div>
                    <div class="category-score">
                        <span>${Math.round(category.percentage)}%</span>
                        <div class="score-bar">
                            <div class="score-fill" style="width: ${category.percentage}%"></div>
                        </div>
                        <span class="score-value">${category.score}/40</span>
                    </div>
                `;
                
                categoryResultsContainer.appendChild(categoryDiv);
            });

            // Test sonucunu veritabanına kaydet
            if (currentUser) {
                // Mevcut test geçmişini al veya yeni dizi oluştur
                const testHistory = currentUser.test_history || [];
                
                // Yeni test sonucunu ekle
                testHistory.push({
                    test_date: new Date().toISOString(),
                    test_results: JSON.stringify(categoryScores),
                    overall_score: Math.round(overallPercentage)
                });

                const updatedUser = {
                    ...currentUser,
                    test_completed: true,
                    test_date: new Date().toISOString(), // En son test tarihi
                    test_results: JSON.stringify(categoryScores), // En son test sonucu (geriye dönük uyumluluk için)
                    overall_score: Math.round(overallPercentage), // En son skor
                    test_history: testHistory // Tüm test geçmişi
                };

                const result = await firebaseDB.update(updatedUser);
                if (result.isOk) {
                    currentUser = updatedUser;
                    allUsers = await firebaseDB.getAll(); // Kullanıcı listesini güncelle
                }
            }
        }

        // Grafik çizim fonksiyonları
        function drawCharts() {
            if (!window.categoryScoresGlobal) return;
            
            // Canvas boyutlarını ayarla
            setCanvasSize();
            
            drawRadarChart();
            drawPieChart();
            drawBarChart();
            drawScatterChart();
        }

        function setCanvasSize() {
            const canvases = ['radarChart', 'pieChart', 'barChart', 'scatterChart'];
            const isMobile = window.innerWidth <= 768;
            const size = isMobile ? 250 : 300;
            
            canvases.forEach(id => {
                const canvas = document.getElementById(id);
                if (canvas) {
                    canvas.width = size;
                    canvas.height = size;
                }
            });
        }

        function drawRadarChart() {
            const canvas = document.getElementById('radarChart');
            const ctx = canvas.getContext('2d');
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const isMobile = window.innerWidth <= 768;
            const radius = Math.min(centerX, centerY) - (isMobile ? 80 : 100);
            
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Arka plan çizgileri
            ctx.strokeStyle = '#e0e0e0';
            ctx.lineWidth = 1;
            for (let i = 1; i <= 5; i++) {
                ctx.beginPath();
                ctx.arc(centerX, centerY, (radius * i) / 5, 0, 2 * Math.PI);
                ctx.stroke();
            }
            
            // Eksen çizgileri ve numaralar
            const angleStep = (2 * Math.PI) / 10;
            for (let i = 0; i < 10; i++) {
                const angle = i * angleStep - Math.PI / 2;
                const x = centerX + Math.cos(angle) * radius;
                const y = centerY + Math.sin(angle) * radius;
                
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.lineTo(x, y);
                ctx.stroke();
                
                // Numara etiketi (1-10)
                ctx.fillStyle = '#667eea';
                ctx.font = 'bold ' + (isMobile ? '14px' : '16px') + ' Arial';
                ctx.textAlign = 'center';
                const numRadius = radius + (isMobile ? 15 : 20);
                const numX = centerX + Math.cos(angle) * numRadius;
                const numY = centerY + Math.sin(angle) * numRadius;
                ctx.fillText((i + 1).toString(), numX, numY + 5);
            }
            
            // Veri çizimi
            ctx.strokeStyle = '#667eea';
            ctx.fillStyle = 'rgba(102, 126, 234, 0.3)';
            ctx.lineWidth = isMobile ? 2 : 3;
            ctx.beginPath();
            
            window.categoryScoresGlobal.forEach((category, index) => {
                const angle = index * angleStep - Math.PI / 2;
                const value = (category.percentage / 100) * radius;
                const x = centerX + Math.cos(angle) * value;
                const y = centerY + Math.sin(angle) * value;
                
                if (index === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
                
                // Veri noktası
                ctx.fillStyle = '#667eea';
                ctx.beginPath();
                ctx.arc(x, y, 4, 0, 2 * Math.PI);
                ctx.fill();
            });
            
            ctx.closePath();
            ctx.fillStyle = 'rgba(102, 126, 234, 0.3)';
            ctx.fill();
            ctx.strokeStyle = '#667eea';
            ctx.stroke();
            
            // Legend (Açıklama) - Canvas dışında HTML ile
            const legendContainer = document.getElementById('radarChartLegend');
            if (legendContainer) {
                let legendHTML = '<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; margin-top: 20px;">';
                window.categoryScoresGlobal.forEach((category, index) => {
                    legendHTML += `
                        <div style="display: flex; align-items: center; gap: 8px; padding: 8px; background: #f9f9f9; border-radius: 6px;">
                            <div style="
                                width: 24px; 
                                height: 24px; 
                                background: #667eea; 
                                border-radius: 50%; 
                                display: flex; 
                                align-items: center; 
                                justify-content: center;
                                color: white;
                                font-weight: bold;
                                font-size: 12px;
                            ">${index + 1}</div>
                            <div style="flex: 1; font-size: 13px;">
                                <strong>${category.name}</strong>
                                <div style="color: #666; font-size: 11px;">${Math.round(category.percentage)}% - ${category.score}/40</div>
                            </div>
                        </div>
                    `;
                });
                legendHTML += '</div>';
                legendContainer.innerHTML = legendHTML;
            }
        }

        function drawPieChart() {
            const canvas = document.getElementById('pieChart');
            const ctx = canvas.getContext('2d');
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const isMobile = window.innerWidth <= 768;
            const radius = Math.min(centerX, centerY) - (isMobile ? 30 : 40);
            
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            const colors = [
                '#667eea', '#764ba2', '#f093fb', '#f5576c', '#4facfe',
                '#43e97b', '#fa709a', '#fee140', '#a8edea', '#d299c2'
            ];
            
            let currentAngle = -Math.PI / 2;
            const total = window.categoryScoresGlobal.reduce((sum, cat) => sum + cat.score, 0);
            
            window.categoryScoresGlobal.forEach((category, index) => {
                const sliceAngle = (category.score / total) * 2 * Math.PI;
                
                ctx.fillStyle = colors[index % colors.length];
                ctx.beginPath();
                ctx.moveTo(centerX, centerY);
                ctx.arc(centerX, centerY, radius, currentAngle, currentAngle + sliceAngle);
                ctx.closePath();
                ctx.fill();
                
                // Numara ve yüzde etiketi - pasta dilimindeki kategori numarası ve payı
                const piePercentage = (category.score / total) * 100;
                const labelAngle = currentAngle + sliceAngle / 2;
                const labelX = centerX + Math.cos(labelAngle) * (radius * 0.7);
                const labelY = centerY + Math.sin(labelAngle) * (radius * 0.7);
                
                ctx.fillStyle = 'white';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                // Numara (üstte)
                ctx.font = isMobile ? 'bold 16px Arial' : 'bold 20px Arial';
                ctx.fillText((index + 1).toString(), labelX, labelY - (isMobile ? 6 : 8));
                
                // Yüzde (altta)
                ctx.font = isMobile ? 'bold 10px Arial' : 'bold 12px Arial';
                ctx.fillText(Math.round(piePercentage) + '%', labelX, labelY + (isMobile ? 6 : 8));
                
                currentAngle += sliceAngle;
            });
            
            // Legend (Açıklama) - HTML ile
            const legendContainer = document.getElementById('pieChartLegend');
            if (legendContainer) {
                let legendHTML = '<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 10px; margin-top: 20px;">';
                window.categoryScoresGlobal.forEach((category, index) => {
                    const piePercentage = (category.score / total) * 100;
                    legendHTML += `
                        <div style="display: flex; align-items: center; gap: 10px; padding: 10px; background: #f9f9f9; border-radius: 8px;">
                            <div style="
                                width: 30px; 
                                height: 30px; 
                                background: ${colors[index % colors.length]}; 
                                border-radius: 6px;
                                flex-shrink: 0;
                                display: flex;
                                align-items: center;
                                justify-content: center;
                                color: white;
                                font-weight: bold;
                                font-size: 14px;
                            ">${index + 1}</div>
                            <div style="flex: 1;">
                                <div style="font-weight: bold; font-size: 13px; margin-bottom: 3px;">${category.name}</div>
                                <div style="color: #666; font-size: 12px;">
                                    Pasta Payı: <strong>${Math.round(piePercentage)}%</strong> | 
                                    Skor: <strong>${category.score}/40</strong> (${Math.round(category.percentage)}%)
                                </div>
                            </div>
                        </div>
                    `;
                });
                legendHTML += '</div>';
                legendContainer.innerHTML = legendHTML;
            }
        }

        function drawBarChart() {
            const canvas = document.getElementById('barChart');
            const ctx = canvas.getContext('2d');
            const isMobile = window.innerWidth <= 768;
            const padding = isMobile ? 40 : 50;
            const bottomPadding = isMobile ? 80 : 100; // Alt için daha fazla alan
            const chartWidth = canvas.width - 2 * padding;
            const chartHeight = canvas.height - padding - bottomPadding;
            
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Eksenler
            ctx.strokeStyle = '#333';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(padding, padding);
            ctx.lineTo(padding, canvas.height - bottomPadding);
            ctx.lineTo(canvas.width - padding, canvas.height - bottomPadding);
            ctx.stroke();
            
            // Çubuklar
            const barWidth = chartWidth / window.categoryScoresGlobal.length - (isMobile ? 5 : 10);
            const maxScore = Math.max(...window.categoryScoresGlobal.map(cat => cat.percentage));
            
            window.categoryScoresGlobal.forEach((category, index) => {
                const barHeight = (category.percentage / 100) * chartHeight;
                const x = padding + index * (chartWidth / window.categoryScoresGlobal.length) + (isMobile ? 2.5 : 5);
                const y = canvas.height - bottomPadding - barHeight;
                
                const gradient = ctx.createLinearGradient(0, y, 0, y + barHeight);
                gradient.addColorStop(0, '#667eea');
                gradient.addColorStop(1, '#764ba2');
                
                ctx.fillStyle = gradient;
                ctx.fillRect(x, y, barWidth, barHeight);
                
                // Değer etiketi (üstte)
                ctx.fillStyle = '#333';
                ctx.font = isMobile ? 'bold 10px Arial' : 'bold 12px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(Math.round(category.percentage) + '%', x + barWidth / 2, y - 5);
                
                // Kategori numarası (altta)
                ctx.fillStyle = '#667eea';
                ctx.font = isMobile ? 'bold 14px Arial' : 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.fillText((index + 1).toString(), x + barWidth / 2, canvas.height - bottomPadding + 20);
            });
            
            // Legend (Açıklama)
            const legendContainer = document.getElementById('barChartLegend');
            if (legendContainer) {
                let legendHTML = '<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; margin-top: 20px;">';
                const colors = [
                    '#667eea', '#764ba2', '#f093fb', '#f5576c', '#4facfe',
                    '#43e97b', '#fa709a', '#fee140', '#a8edea', '#d299c2'
                ];
                window.categoryScoresGlobal.forEach((category, index) => {
                    legendHTML += `
                        <div style="display: flex; align-items: center; gap: 8px; padding: 8px; background: #f9f9f9; border-radius: 6px;">
                            <div style="
                                width: 24px; 
                                height: 24px; 
                                background: linear-gradient(135deg, #667eea, #764ba2); 
                                border-radius: 4px; 
                                display: flex; 
                                align-items: center; 
                                justify-content: center;
                                color: white;
                                font-weight: bold;
                                font-size: 12px;
                            ">${index + 1}</div>
                            <div style="flex: 1; font-size: 13px;">
                                <strong>${category.name}</strong>
                                <div style="color: #666; font-size: 11px;">${Math.round(category.percentage)}% - ${category.score}/40</div>
                            </div>
                        </div>
                    `;
                });
                legendHTML += '</div>';
                legendContainer.innerHTML = legendHTML;
            }
        }

        function drawScatterChart() {
            const canvas = document.getElementById('scatterChart');
            const ctx = canvas.getContext('2d');
            const isMobile = window.innerWidth <= 768;
            const padding = isMobile ? 30 : 40;
            const chartWidth = canvas.width - 2 * padding;
            const chartHeight = canvas.height - 2 * padding;
            
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Eksenler
            ctx.strokeStyle = '#333';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(padding, padding);
            ctx.lineTo(padding, canvas.height - padding);
            ctx.lineTo(canvas.width - padding, canvas.height - padding);
            ctx.stroke();
            
            // Grid çizgileri ve Y ekseni etiketleri
            ctx.strokeStyle = '#e0e0e0';
            ctx.lineWidth = 1;
            ctx.fillStyle = '#666';
            ctx.font = '10px Arial';
            ctx.textAlign = 'right';
            
            for (let i = 0; i <= 5; i++) {
                const y = padding + (chartHeight * i) / 5;
                const label = 100 - (i * 20);
                
                ctx.beginPath();
                ctx.moveTo(padding, y);
                ctx.lineTo(canvas.width - padding, y);
                ctx.stroke();
                
                ctx.fillText(label + '%', padding - 5, y + 4);
            }
            
            // X ekseni etiketleri (kategori numaraları)
            ctx.textAlign = 'center';
            ctx.fillStyle = '#667eea';
            ctx.font = 'bold 11px Arial';
            
            // Noktalar ve bağlantılar
            const dotRadius = isMobile ? 6 : 8;
            const colors = [
                '#667eea', '#764ba2', '#f093fb', '#f5576c', '#4facfe',
                '#43e97b', '#fa709a', '#fee140', '#a8edea', '#d299c2'
            ];
            
            window.categoryScoresGlobal.forEach((category, index) => {
                const x = padding + (index / (window.categoryScoresGlobal.length - 1)) * chartWidth;
                const y = canvas.height - padding - (category.percentage / 100) * chartHeight;
                
                // X ekseni numarası
                ctx.fillStyle = '#667eea';
                ctx.fillText((index + 1).toString(), x, canvas.height - padding + 15);
                
                // Nokta
                const gradient = ctx.createRadialGradient(x, y, 0, x, y, dotRadius);
                gradient.addColorStop(0, colors[index % colors.length]);
                gradient.addColorStop(1, '#764ba2');
                
                ctx.fillStyle = gradient;
                ctx.beginPath();
                ctx.arc(x, y, dotRadius, 0, 2 * Math.PI);
                ctx.fill();
                
                // Skor etiketi
                ctx.fillStyle = '#333';
                ctx.font = 'bold 10px Arial';
                ctx.fillText(Math.round(category.percentage) + '%', x, y - 12);
                
                // Çizgi bağlantısı
                if (index > 0) {
                    const prevX = padding + ((index - 1) / (window.categoryScoresGlobal.length - 1)) * chartWidth;
                    const prevY = canvas.height - padding - (window.categoryScoresGlobal[index - 1].percentage / 100) * chartHeight;
                    
                    ctx.strokeStyle = 'rgba(102, 126, 234, 0.5)';
                    ctx.lineWidth = isMobile ? 1.5 : 2;
                    ctx.beginPath();
                    ctx.moveTo(prevX, prevY);
                    ctx.lineTo(x, y);
                    ctx.stroke();
                }
            });
            
            // Legend (Açıklama)
            const legendContainer = document.getElementById('scatterChartLegend');
            if (legendContainer) {
                let legendHTML = '<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 10px; margin-top: 20px;">';
                window.categoryScoresGlobal.forEach((category, index) => {
                    legendHTML += `
                        <div style="display: flex; align-items: center; gap: 8px; padding: 8px; background: #f9f9f9; border-radius: 6px;">
                            <div style="
                                width: 24px; 
                                height: 24px; 
                                background: ${colors[index % colors.length]}; 
                                border-radius: 50%; 
                                display: flex; 
                                align-items: center; 
                                justify-content: center;
                                color: white;
                                font-weight: bold;
                                font-size: 12px;
                            ">${index + 1}</div>
                            <div style="flex: 1; font-size: 13px;">
                                <strong>${category.name}</strong>
                                <div style="color: #666; font-size: 11px;">${Math.round(category.percentage)}%</div>
                            </div>
                        </div>
                    `;
                });
                legendHTML += '</div>';
                legendContainer.innerHTML = legendHTML;
            }
        }

        // Analiz oluşturma fonksiyonu
        function generateAnalyses() {
            if (!window.categoryScoresGlobal) return;
            
            const analysesContainer = document.getElementById('categoryAnalyses');
            analysesContainer.innerHTML = '';
            
            window.categoryScoresGlobal.forEach(category => {
                const analysisDiv = document.createElement('div');
                analysisDiv.className = 'category-analysis';
                
                const scoreClass = getScoreClass(category.percentage);
                
                // Gelişmiş AI analiz metni oluştur
                const aiAnalysis = generateAdvancedAIAnalysis(category.name, category.percentage, category.score);
                
                analysisDiv.innerHTML = `
                    <h4>${category.name} <span class="score-badge ${scoreClass}">${Math.round(category.percentage)}%</span></h4>
                    ${aiAnalysis}
                `;
                
                analysesContainer.appendChild(analysisDiv);
            });
        }

        // Gelişmiş AI Analiz Motoru
        function generateAdvancedAIAnalysis(categoryName, percentage, rawScore) {
            const scoreLevel = getScoreLevel(percentage);
            const userInfo = {
                education: currentUser.education_level,
                department: currentUser.department,
                position: currentUser.current_position
            };

            // Her kategori için özel analiz parametreleri
            const categoryContext = getCategoryContext(categoryName, percentage, rawScore, userInfo);
            
            return `
                <div class="ai-analysis-box">
                    <div class="ai-analysis-title">
                        🤖 AKÇA PRO X AI ANALİZİ 
                    </div>
                    
                    <div class="analysis-subsection">
                        <h5>📊 Performans Değerlendirmesi</h5>
                        <p>${categoryContext.performanceEvaluation}</p>
                    </div>

                    <div class="analysis-subsection">
                        <h5>🎯 Mevcut Durum Analizi</h5>
                        <p>${categoryContext.currentSituation}</p>
                    </div>

                    <div class="analysis-subsection">
                        <h5>💡 Gelişim Potansiyeli</h5>
                        <p>${categoryContext.developmentPotential}</p>
                    </div>

                    <div class="analysis-subsection">
                        <h5>🚀 Önerilen Eylem Planı</h5>
                        <ul>
                            ${categoryContext.actionPlan.map(action => `<li>${action}</li>`).join('')}
                        </ul>
                    </div>

                    <div class="analysis-subsection">
                        <h5>📚 Öğrenme Kaynakları ve Araçlar</h5>
                        <ul>
                            ${categoryContext.resources.map(resource => `<li>${resource}</li>`).join('')}
                        </ul>
                    </div>

                    <div class="analysis-subsection">
                        <h5>⏱️ Tahmini Gelişim Süresi</h5>
                        <p>${categoryContext.timeframe}</p>
                    </div>

                    <div class="analysis-subsection">
                        <h5>🎓 Kariyer Etkisi</h5>
                        <p>${categoryContext.careerImpact}</p>
                    </div>
                </div>
            `;
        }

        // Skor seviyesi belirleme
        function getScoreLevel(percentage) {
            if (percentage >= 90) return 'outstanding';
            if (percentage >= 85) return 'excellent';
            if (percentage >= 75) return 'veryGood';
            if (percentage >= 65) return 'good';
            if (percentage >= 55) return 'average';
            if (percentage >= 45) return 'belowAverage';
            return 'needsImprovement';
        }

        // Kategori bağlamı oluşturma - Ana analiz motoru
        function getCategoryContext(categoryName, percentage, rawScore, userInfo) {
            const scoreLevel = getScoreLevel(percentage);
            const contexts = {
                "Stratejik Kariyer Planlaması": generateStrategicPlanningAnalysis(percentage, scoreLevel, userInfo),
                "Etkili İletişim ve Sunum": generateCommunicationAnalysis(percentage, scoreLevel, userInfo),
                "Problem Çözme ve Kritik Düşünme": generateProblemSolvingAnalysis(percentage, scoreLevel, userInfo),
                "Zaman ve Enerji Yönetimi": generateTimeManagementAnalysis(percentage, scoreLevel, userInfo),
                "Öz Liderlik ve Sorumluluk": generateSelfLeadershipAnalysis(percentage, scoreLevel, userInfo),
                "Ekip Çalışması ve Çatışma Yönetimi": generateTeamworkAnalysis(percentage, scoreLevel, userInfo),
                "Öğrenme Çevikliği": generateLearningAgilityAnalysis(percentage, scoreLevel, userInfo),
                "Duygusal Zeka ve Stres Toleransı": generateEmotionalIntelligenceAnalysis(percentage, scoreLevel, userInfo),
                "Profesyonel Marka ve Ağ Yönetimi": generateNetworkingAnalysis(percentage, scoreLevel, userInfo),
                "Yenilikçilik ve Geliştirme Odaklılık": generateInnovationAnalysis(percentage, scoreLevel, userInfo)
            };

            return contexts[categoryName] || generateDefaultAnalysis(percentage, scoreLevel, userInfo);
        }

        // Stratejik Kariyer Planlaması Analizi
        function generateStrategicPlanningAnalysis(percentage, level, userInfo) {
            const analyses = {
                outstanding: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz mükemmel seviyede. Stratejik planlama konusunda çok güçlüsünüz.`,
                    currentSituation: `Uzun vadeli planlama, risk analizi ve hedef belirleme becerileriniz oldukça gelişmiş durumda.`,
                    developmentPotential: `Liderlik ve mentorluk rolleri için hazırsınız. Stratejik projelerde sorumluluk alabilirsiniz.`,
                    actionPlan: [
                        "Sektör etkinliklerinde sunum yapın",
                        "LinkedIn'de içerik paylaşarak görünürlük kazanın",
                        "Mentorluk yaparak deneyim aktarın"
                    ],
                    resources: [
                        "HBR Türkiye - Stratejik makaleler",
                        "Coursera, Udemy - Online kurslar",
                        "LinkedIn Learning"
                    ],
                    timeframe: `12-18 ayda takım liderliği ve yöneticilik pozisyonlarına hazır olabilirsiniz.`,
                    careerImpact: `Bu yetkinlik terfi ve kariyer gelişimi için önemli bir avantaj sağlar.`
                },
                excellent: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz çok iyi seviyede. Stratejik düşünme becerileriniz güçlü.`,
                    currentSituation: `Planlama, analiz ve hedef belirleme konularında yetkinsiniz.`,
                    developmentPotential: `Kıdemli uzman ve takım liderliği için uygun bir temel var.`,
                    actionPlan: [
                        "Vaka çalışmaları yapın",
                        "Farklı departmanlarda proje deneyimi kazanın",
                        "Mentorluk desteği alın"
                    ],
                    resources: [
                        "Coursera - Stratejik Düşünme",
                        "LinkedIn Learning",
                        "SWOT, PESTEL analiz araçları"
                    ],
                    timeframe: `12-24 ay içinde yöneticilik pozisyonlarına hazır olabilirsiniz.`,
                    careerImpact: `Kariyer gelişiminizi hızlandırma potansiyeliniz yüksek.`
                },
                veryGood: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz iyi seviyede. Gelişime açık bir profiliniz var.`,
                    currentSituation: `Temel planlama ve analiz becerileri mevcut, derinleştirilebilir.`,
                    developmentPotential: `Sistematik çalışmayla yönetim pozisyonlarına geçiş yapabilirsiniz.`,
                    actionPlan: [
                        "Stratejik planlama eğitimleri alın",
                        "SWOT analizi yapma pratiği kazanın",
                        "Kariyer planı oluşturun ve takip edin"
                    ],
                    resources: [
                        "Udemy - Stratejik Planlama",
                        "HBR makaleleri",
                        "Planlama araçları ve şablonlar"
                    ],
                    timeframe: `18-24 ayda önemli gelişim gösterebilirsiniz.`,
                    careerImpact: `Bu alanda gelişim terfi şansınızı artırır.`
                },
                good: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz orta seviyede. Gelişim potansiyeliniz var.`,
                    currentSituation: `Kısa vadeli planlama yapabiliyorsunuz, stratejik düşünme gelişmeli.`,
                    developmentPotential: `Eğitim ve pratikle 12-18 ayda önemli ilerleme kaydedebilirsiniz.`,
                    actionPlan: [
                        "Temel stratejik düşünme eğitimleri alın",
                        "SMART hedefler belirleyin",
                        "Mentorluk desteği alın"
                    ],
                    resources: [
                        "YouTube - Ücretsiz kurslar",
                        "Coursera başlangıç seviyesi",
                        "Kariyer planlama araçları"
                    ],
                    timeframe: `6-12 ayda temel becerileri kazanabilirsiniz.`,
                    careerImpact: `Bu alana yatırım yapmanız kariyer gelişiminiz için önemli.`
                },
                average: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz düşük seviyede. Acil gelişim gerekli.`,
                    currentSituation: `Uzun vadeli planlama yapamıyorsunuz, reaktif yaklaşım sergiliyorsunuz.`,
                    developmentPotential: `Koçluk desteği ile 6-12 ayda temel becerileri kazanabilirsiniz.`,
                    actionPlan: [
                        "Kariyer koçu ile çalışın",
                        "Hedef belirleme eğitimleri alın",
                        "Kısa vadeli planlar yapın"
                    ],
                    resources: [
                        "Kariyer danışmanlığı",
                        "LinkedIn Learning temel kursları",
                        "Basit planlama araçları"
                    ],
                    timeframe: `6-12 ayda temel becerileri kazanmayı hedefleyin.`,
                    careerImpact: `Bu eksiklik kariyer gelişiminizi engelliyor, acil çalışma gerekli.`
                }
            };

            return analyses[level] || analyses.average;
        }

        // Diğer kategoriler için benzer detaylı analiz fonksiyonları...
        // (Karakter limiti nedeniyle sadece bir örnek gösterildi, diğerleri benzer yapıda olacak)

        function generateCommunicationAnalysis(percentage, level, userInfo) {
            const baseAnalyses = {
                outstanding: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz mükemmel. İletişim ve sunum becerileriniz çok güçlü.`,
                    currentSituation: `Etkili sunum, aktif dinleme ve net ifade yetenekleriniz gelişmiş durumda.`,
                    developmentPotential: `Eğitim verme, proje sunumları ve paydaş yönetiminde liderlik yapabilirsiniz.`,
                    actionPlan: ["Etkinliklerde sunum yapın", "Toastmasters'a katılın", "LinkedIn'de içerik paylaşın"],
                    resources: ["Coursera/Udemy - İletişim kursları", "Toastmasters", "LinkedIn Learning"],
                    timeframe: `12-18 ayda sektörünüzde tanınırlık kazanabilirsiniz.`,
                    careerImpact: `İletişim gücünüz kariyer gelişiminde büyük avantaj sağlar.`
                },
                excellent: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz çok iyi. Etkili iletişim kuruyorsunuz.`,
                    currentSituation: `Net ifade, empati ve sunum becerileriniz gelişmiş.`,
                    developmentPotential: `Ekip liderliği ve proje yönetiminde başarılı olabilirsiniz.`,
                    actionPlan: ["Sunum atölyelerine katılın", "Çatışma yönetimi eğitimi alın", "Yazılı iletişimi geliştirin"],
                    resources: ["Coursera İletişim", "Toastmasters", "LinkedIn Learning"],
                    timeframe: `12-18 ayda yöneticilik için hazır olabilirsiniz.`,
                    careerImpact: `İletişim yetkinliği terfi kararlarında önemli rol oynar.`
                },
                veryGood: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz iyi. Gelişim potansiyeli var.`,
                    currentSituation: `Günlük iletişimde iyisiniz, sunum becerileri geliştirilebilir.`,
                    developmentPotential: `Eğitim ve pratikle liderlik düzeyine ulaşabilirsiniz.`,
                    actionPlan: ["Sunum eğitimleri alın", "Toastmasters pratiği yapın", "Geri bildirim becerisi geliştirin"],
                    resources: ["Udemy Sunum Kursları", "TED Masterclass", "Coursera"],
                    timeframe: `12-18 ayda önemli gelişim gösterebilirsiniz.`,
                    careerImpact: `İletişim becerisi kariyer gelişimini hızlandırır.`
                },
                good: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz orta. Gelişim gerekli.`,
                    currentSituation: `Birebir iletişimde rahat, grup sunumlarında gelişim şart.`,
                    developmentPotential: `6-12 ayda önemli ilerleme kaydedebilirsiniz.`,
                    actionPlan: ["Temel sunum eğitimi alın", "Email yazma kursları", "Küçük gruplarla pratik yapın"],
                    resources: ["LinkedIn Learning", "Coursera Başlangıç", "YouTube ücretsiz"],
                    timeframe: `6-12 ayda profesyonel seviyeye ulaşabilirsiniz.`,
                    careerImpact: `Bu alana yatırım yapmanız kritik önemde.`
                },
                average: {
                    performanceEvaluation: `%${Math.round(percentage)} skorunuz düşük. Acil gelişim gerekli.`,
                    currentSituation: `İletişimde güven eksikliği ve sunum kaygısı yaşıyorsunuz.`,
                    developmentPotential: `Koçluk desteği ile 6-12 ayda temel becerileri kazanabilirsiniz.`,
                    actionPlan: ["İletişim koçu ile çalışın", "Özgüven geliştirme", "Küçük gruplarda pratik"],
                    resources: ["İletişim koçluğu", "Dale Carnegie kitapları", "Toastmasters"],
                    timeframe: `6-12 ayda temel seviyeye ulaşmayı hedefleyin.`,
                    careerImpact: `İletişim eksikliği kariyer gelişimini engelliyor, acil çalışma şart.`
                }
            };
            return baseAnalyses[level] || baseAnalyses.average;
        }

        // Kısa versiyonları ekleyelim (diğer 8 kategori için)
        function generateProblemSolvingAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Problem Çözme ve Kritik Düşünme', percentage, level, userInfo, {
                keySkills: ['analitik düşünme', 'kök neden analizi', 'yaratıcı çözüm geliştirme', 'veri analizi'],
                careerRelevance: 'Stratejik roller, proje yönetimi, danışmanlık'
            });
        }

        function generateTimeManagementAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Zaman ve Enerji Yönetimi', percentage, level, userInfo, {
                keySkills: ['önceliklendirme', 'verimlilik', 'delegasyon', 'enerji optimizasyonu'],
                careerRelevance: 'Tüm yönetim seviyeleri, liderlik rolleri'
            });
        }

        function generateSelfLeadershipAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Öz Liderlik ve Sorumluluk', percentage, level, userInfo, {
                keySkills: ['öz disiplin', 'sorumluluk alma', 'sürekli gelişim', 'değer temelli liderlik'],
                careerRelevance: 'Üst düzey yöneticilik, girişimcilik, takım liderliği'
            });
        }

        function generateTeamworkAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Ekip Çalışması ve Çatışma Yönetimi', percentage, level, userInfo, {
                keySkills: ['işbirliği', 'çatışma çözme', 'ekip dinamikleri', 'kapsayıcı liderlik'],
                careerRelevance: 'Takım liderliği, proje yönetimi, farklı departmanlarla çalışma'
            });
        }

        function generateLearningAgilityAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Öğrenme Çevikliği', percentage, level, userInfo, {
                keySkills: ['hızlı öğrenme', 'adaptasyon', 'bilgi transferi', 'sürekli gelişim'],
                careerRelevance: 'Teknoloji rolleri, değişim yönetimi, inovasyon'
            });
        }

        function generateEmotionalIntelligenceAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Duygusal Zeka ve Stres Toleransı', percentage, level, userInfo, {
                keySkills: ['empati', 'duygusal düzenleme', 'stres yönetimi', 'sosyal farkındalık'],
                careerRelevance: 'Liderlik, müşteri ilişkileri, insan kaynakları'
            });
        }

        function generateNetworkingAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Profesyonel Marka ve Ağ Yönetimi', percentage, level, userInfo, {
                keySkills: ['networking', 'kişisel marka', 'ilişki yönetimi', 'görünürlük'],
                careerRelevance: 'Business development, liderlik, girişimcilik'
            });
        }

        function generateInnovationAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Yenilikçilik ve Geliştirme Odaklılık', percentage, level, userInfo, {
                keySkills: ['yaratıcılık', 'inovasyon', 'sürekli iyileştirme', 'trend analizi'],
                careerRelevance: 'İnovasyon rolleri, R&D, stratejik planlama'
            });
        }

        // Genel kategori analizi oluşturucu
        function getGenericCategoryAnalysis(categoryName, percentage, level, userInfo, specs) {
            const performanceDescriptors = {
                outstanding: 'seçkin', excellent: 'mükemmel', veryGood: 'çok iyi',
                good: 'iyi', average: 'gelişmeye açık', belowAverage: 'yetersiz', needsImprovement: 'acil gelişim gerektiren'
            };

            return {
                performanceEvaluation: `${categoryName} alanında %${Math.round(percentage)}'lik performansınız, ${performanceDescriptors[level]} bir seviyeyi temsil etmektedir. ${userInfo.position} pozisyonunuzda bu yetkinlik, ${userInfo.department} alanındaki profesyonel gelişiminiz için ${level === 'outstanding' || level === 'excellent' ? 'güçlü bir avantaj' : 'önemli bir gelişim alanı'} oluşturmaktadır.`,
                
                currentSituation: `Mevcut durumunuz ${specs.keySkills.join(', ')} gibi temel becerilerde ${level === 'outstanding' || level === 'excellent' ? 'üstün bir performans' : level === 'veryGood' || level === 'good' ? 'gelişmeye açık bir yapı' : 'sistematik gelişim ihtiyacı'} sergilemektedir. ${userInfo.education} mezuniyetinizin sağladığı akademik altyapı ile birleştiğinde, bu yetkinlik ${specs.careerRelevance} alanlarında belirleyici olmaktadır.`,
                
                developmentPotential: `${level === 'outstanding' || level === 'excellent' ? 'Bu üstün performansınızı sürdürerek, sektörünüzde düşünce lideri konumuna ulaşabilir ve mentorship rolleri üstlenebilirsiniz.' : level === 'veryGood' || level === 'good' ? 'Yapılandırılmış gelişim programları ile 12-18 ay içinde bu alanda üst seviye yetkinliğe ulaşabilirsiniz.' : 'Profesyonel destek ve yoğun çalışma ile 6-12 ay içinde temel yetkinlikleri kazanmanız mümkündür.'}`,
                
                actionPlan: level === 'outstanding' || level === 'excellent' ? [
                    `${categoryName} alanında sertifikasyon ve ileri eğitim programları tamamlayın`,
                    `Sektör konferanslarında ${specs.keySkills[0]} konusunda sunumlar yapın`,
                    `Genç profesyonellere mentorluk yaparak bilginizi paylaşın`,
                    `Akademik makaleler ve blog yazıları yayımlayarak düşünce liderliği konumunuzu güçlendirin`,
                    `Uluslararası ağ oluşturma ve bilgi paylaşım platformlarında aktif olun`
                ] : level === 'veryGood' || level === 'good' ? [
                    `${specs.keySkills[0]} ve ${specs.keySkills[1]} becerileri üzerine eğitimler alın`,
                    `Pratik projeler ve örnek çalışmalar üzerinde çalışarak deneyim kazanın`,
                    `Profesyonel gelişim programlarına düzenli katılın`,
                    `Mentor desteği alarak hızlı gelişim sağlayın`,
                    `Online kurslar ve sertifikasyonlarla bilginizi güncel tutun`
                ] : [
                    `Temel ${specs.keySkills[0]} eğitimlerinden başlayın`,
                    `Profesyonel koçluk veya danışmanlık desteği alın`,
                    `Küçük projelerle pratik deneyim kazanmaya başlayın`,
                    `Akran öğrenme gruplarına katılın`,
                    `Düzenli öz değerlendirme yaparak ilerlemenizi takip edin`
                ],
                
                resources: level === 'outstanding' || level === 'excellent' ? [
                    `Üst düzey yönetici eğitim programları - Harvard, Stanford, INSEAD`,
                    `Profesyonel sertifikasyon: ${specs.careerRelevance} alanında ileri seviye`,
                    `Sektör lideri uzmanlık kursları ve atölyeler`,
                    `Önde gelen danışmanlık firmalarının araştırma yayınları`,
                    `Küresel profesyonel dernekler ve düşünce liderliği platformları`
                ] : level === 'veryGood' || level === 'good' ? [
                    `Coursera/edX: ${categoryName} konusunda uzmanlaşma kursları`,
                    `LinkedIn Learning profesyonel gelişim programları`,
                    `Sektöre özel sertifika ve eğitim programları`,
                    `Profesyonel kitaplar ve sektör makaleleri`,
                    `Ağ oluşturma etkinlikleri ve mesleki buluşmalar`
                ] : [
                    `Temel online kurslar - Udemy, Coursera temel seviye`,
                    `YouTube eğitim kanalları (ücretsiz kaynaklar)`,
                    `Başlangıç seviyesi kitaplar ve rehberler`,
                    `Yerel atölyeler ve topluluk öğrenme grupları`,
                    `Profesyonel koçluk seansları`
                ],
                
                timeframe: level === 'outstanding' || level === 'excellent' ? 
                    `Bu üstün seviyenizi sürdürmek ve küresel tanınırlık kazanmak için 12-24 aylık stratejik görünürlük ve düşünce liderliği planı önerilir. Üst düzey eğitim ve uluslararası deneyime öncelik verilmelidir.` :
                    level === 'veryGood' || level === 'good' ?
                    `Kıdemli uzman veya yönetici pozisyonları için gereken yetkinlik seviyesine 12-18 ay içinde ulaşabilirsiniz. İlk 6 ayda temel becerileri pekiştirmeye, sonraki 6-12 ayda ileri tekniklere odaklanılmalıdır.` :
                    `İlk 3-6 ayda temel becerileri kazanmak, 6-12 ay içinde profesyonel ortamlarda rahat çalışabilir seviyeye ulaşmak hedeflenmelidir. Düzenli koçluk ve mentorluk desteği kritik öneme sahiptir.`,
                
                careerImpact: level === 'outstanding' || level === 'excellent' ?
                    `${categoryName} alanındaki bu üstün performansınız, üst düzey yönetici pozisyonlarına geçişte %60-70 avantaj sağlamaktadır. Bu yetkinlik, insan kaynakları uzmanlarının ve iş arama firmalarının en çok aradığı özelliklerdendir. Küresel şirketlerde liderlik rolleri için ideal profile sahipsiniz.` :
                    level === 'veryGood' || level === 'good' ?
                    `Bu yetkinlik seviyeniz, orta ve üst kademe pozisyonlarına geçişte %40-50 avantaj sağlar. Sistematik gelişim ile 2-3 yıl içinde liderlik pozisyonlarına ulaşma olasılığınız yüksektir. ${specs.careerRelevance} alanlarında belirgin fırsatlar yaratır.` :
                    `${categoryName} becerilerindeki eksiklik, kariyer ilerlemenizi doğrudan etkilemektedir. Bu alan modern iş dünyasında ${specs.careerRelevance} için kritik öneme sahip olduğundan, acil ve yoğun gelişim programına ihtiyaç vardır. 6-12 aylık yapılandırılmış eğitim ile önemli ilerleme kaydetmeniz mümkündür.`
            };
        }

        function generateDefaultAnalysis(percentage, level, userInfo) {
            return getGenericCategoryAnalysis('Bu Kategori', percentage, level, userInfo, {
                keySkills: ['temel beceriler', 'profesyonel yetkinlikler'],
                careerRelevance: 'Genel kariyer gelişimi'
            });
        }

        function getScoreClass(percentage) {
            if (percentage >= 85) return 'score-excellent';
            if (percentage >= 70) return 'score-good';
            if (percentage >= 55) return 'score-average';
            return 'score-needs-improvement';
        }

        function getCategoryAnalysis(categoryName, percentage) {
            const analyses = {
                "Stratejik Kariyer Planlaması": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Kariyer planlamanızda stratejik düşünce ve uzun vadeli vizyon sahibisiniz. Hedeflerinizi net olarak tanımlayabilir ve bu hedeflere ulaşmak için sistematik yaklaşımlar geliştirebilirsiniz.</p><p><strong>Güçlü Yönler:</strong> Risk-fayda analizi, kaynak planlaması ve adaptif strateji geliştirme konularında üst düzey yetkinlik.</p><p><strong>Öneriler:</strong> Bu güçlü yönünüzü başkalarına mentorluk yaparak paylaşabilir, sektörünüzde düşünce liderliği pozisyonu geliştirebilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Kariyer planlamanızda sistematik yaklaşım benimsiyor, orta ve uzun vadeli hedefler belirleyebiliyorsunuz. Çoğu durumda etkili stratejiler geliştirebilirsiniz.</p><p><strong>Gelişim Alanları:</strong> Belirsizlik yönetimi ve değişken koşullara adaptasyon konularında iyileştirme fırsatları mevcut.</p><p><strong>Öneriler:</strong> Senaryo planlama teknikleri öğrenerek, daha esnek kariyer stratejileri geliştirebilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel kariyer planlama becerileriniz mevcut ancak daha sistematik ve stratejik yaklaşım geliştirme ihtiyacınız var.</p><p><strong>Gelişim Alanları:</strong> Uzun vadeli vizyon oluşturma, risk değerlendirme ve kaynak planlaması konularında çalışma gerekli.</p><p><strong>Öneriler:</strong> Kariyer koçluğu alarak, SMART hedef belirleme ve stratejik planlama eğitimleri almanızı öneririz.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Kariyer planlamanızda daha proaktif ve sistematik yaklaşım geliştirmeniz kritik önemde.</p><p><strong>Acil Gelişim Alanları:</strong> Hedef belirleme, strateji geliştirme ve uzun vadeli düşünme becerilerinin güçlendirilmesi gerekli.</p><p><strong>Öneriler:</strong> Profesyonel kariyer danışmanlığı alarak, temel planlama becerilerini geliştirmeye odaklanın.</p>"
                },
                "Etkili İletişim ve Sunum": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> İletişim becerileriniz üst düzeyde. Farklı hedef kitlelerle etkili iletişim kurabilir, karmaşık konuları anlaşılır şekilde aktarabilirsiniz.</p><p><strong>Güçlü Yönler:</strong> Aktif dinleme, empati kurma, çatışma yönetimi ve ikna etme becerilerinde uzman seviye.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi liderlik rollerinde kullanarak, ekip iletişimini optimize edebilir ve organizasyonel etkinliği artırabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> İletişim becerileriniz güçlü, çoğu durumda etkili iletişim kurabiliyorsunuz. Sunum ve yazılı iletişimde yetkin seviyedesiniz.</p><p><strong>Gelişim Alanları:</strong> Çatışmalı durumlarda iletişim ve farklı kültürlerle etkileşim konularında iyileştirme fırsatları var.</p><p><strong>Öneriler:</strong> Çatışma çözme teknikleri ve kültürlerarası iletişim eğitimleri alarak becerilerinizi geliştirebilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel iletişim becerileriniz mevcut ancak daha etkili ve profesyonel iletişim için gelişim gerekli.</p><p><strong>Gelişim Alanları:</strong> Sunum teknikleri, yazılı iletişim ve geri bildirim verme konularında çalışma ihtiyacı var.</p><p><strong>Öneriler:</strong> İletişim becerileri eğitimleri alarak, günlük pratikte bu teknikleri uygulayın.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> İletişim becerilerinizin güçlendirilmesi kariyer gelişiminiz için kritik öneme sahip.</p><p><strong>Acil Gelişim Alanları:</strong> Temel iletişim becerileri, dinleme teknikleri ve net ifade etme yeteneği.</p><p><strong>Öneriler:</strong> Temel iletişim eğitimleri alarak, günlük yaşamda bilinçli iletişim pratiği yapın.</p>"
                },
                "Problem Çözme ve Kritik Düşünme": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Analitik düşünme ve problem çözme becerileriniz üst düzeyde. Karmaşık problemleri sistematik olarak analiz edebilir ve yaratıcı çözümler geliştirebilirsiniz.</p><p><strong>Güçlü Yönler:</strong> Kök neden analizi, sistem düşüncesi ve eleştirel değerlendirme konularında uzman seviye.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi stratejik projelerde kullanarak, organizasyonel problem çözme kapasitesini artırabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Problem çözme yaklaşımınız sistematik ve etkili. Çoğu durumda uygun çözümler geliştirebiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Belirsizlik durumlarında karar verme ve yaratıcı çözüm geliştirme konularında iyileştirme fırsatları mevcut.</p><p><strong>Öneriler:</strong> Tasarım düşüncesi ve yaratıcı problem çözme metodolojileri öğrenerek becerilerinizi geliştirebilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel problem çözme becerileriniz var ancak daha sistematik ve yaratıcı yaklaşımlar geliştirme ihtiyacınız bulunuyor.</p><p><strong>Gelişim Alanları:</strong> Analitik düşünme, veri analizi ve alternatif çözüm geliştirme konularında çalışma gerekli.</p><p><strong>Öneriler:</strong> Problem çözme teknikleri eğitimleri alarak, günlük problemlerde bu yöntemleri uygulayın.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Problem çözme ve kritik düşünme becerilerinizin geliştirilmesi acil öncelik taşıyor.</p><p><strong>Acil Gelişim Alanları:</strong> Temel analiz becerileri, mantıklı düşünme ve sistematik yaklaşım geliştirme.</p><p><strong>Öneriler:</strong> Temel mantık ve analitik düşünme eğitimleri alarak, günlük karar verme süreçlerinizi iyileştirin.</p>"
                },
                "Zaman ve Enerji Yönetimi": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Zaman ve enerji yönetiminiz üst düzeyde. Önceliklendirme, planlama ve verimlilik konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> Değer odaklı önceliklendirme, enerji optimizasyonu ve iş-yaşam entegrasyonu konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu becerilerinizi ekip yönetiminde kullanarak, organizasyonel verimliliği artırabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Zaman yönetiminiz etkili, çoğu durumda verimli çalışabiliyorsunuz. Planlama ve önceliklendirme konularında yetkinsiniz.</p><p><strong>Gelişim Alanları:</strong> Enerji yönetimi ve kesinti kontrolü konularında iyileştirme fırsatları var.</p><p><strong>Öneriler:</strong> Derin çalışma teknikleri ve enerji optimizasyonu yöntemleri öğrenerek verimliliğinizi artırabilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel zaman yönetimi becerileriniz mevcut ancak daha etkili ve sistematik yaklaşımlar geliştirme ihtiyacınız var.</p><p><strong>Gelişim Alanları:</strong> Önceliklendirme, planlama ve dikkat yönetimi konularında çalışma gerekli.</p><p><strong>Öneriler:</strong> Zaman yönetimi teknikleri eğitimleri alarak, günlük rutinlerinizi optimize edin.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Zaman ve enerji yönetiminizin iyileştirilmesi verimliliğiniz için kritik önemde.</p><p><strong>Acil Gelişim Alanları:</strong> Temel planlama becerileri, öncelik belirleme ve odaklanma teknikleri.</p><p><strong>Öneriler:</strong> Temel zaman yönetimi eğitimleri alarak, günlük alışkanlıklarınızı yeniden düzenleyin.</p>"
                },
                "Öz Liderlik ve Sorumluluk": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Öz liderlik becerileriniz üst düzeyde. Kişisel gelişim, sorumluluk alma ve otantik liderlik konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> Değer temelli liderlik, sürekli öğrenme zihniyeti ve dayanıklılık geliştirme konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu güçlü yönlerinizi mentorluk ve liderlik rollerinde kullanarak başkalarının gelişimine katkı sağlayabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Öz liderlik becerileriniz güçlü, kişisel gelişim konusunda bilinçli yaklaşım sergiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Öz disiplin ve stres yönetimi konularında iyileştirme fırsatları mevcut.</p><p><strong>Öneriler:</strong> Dayanıklılık geliştirme teknikleri ve alışkanlık oluşturma yöntemleri öğrenerek kendinizi geliştirebilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel öz liderlik becerileriniz var ancak daha sistematik kişisel gelişim yaklaşımı geliştirme ihtiyacınız bulunuyor.</p><p><strong>Gelişim Alanları:</strong> Hedef belirleme, öz disiplin ve geri bildirim alma konularında çalışma gerekli.</p><p><strong>Öneriler:</strong> Kişisel gelişim planı oluşturarak, düzenli öz değerlendirme yapın.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Öz liderlik becerilerinizin geliştirilmesi kişisel ve profesyonel başarınız için kritik öneme sahip.</p><p><strong>Acil Gelişim Alanları:</strong> Sorumluluk alma, öz farkındalık ve temel liderlik becerileri.</p><p><strong>Öneriler:</strong> Kişisel gelişim koçluğu alarak, temel liderlik becerilerini geliştirmeye odaklanın.</p>"
                },
                "Ekip Çalışması ve Çatışma Yönetimi": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Ekip çalışması ve çatışma yönetimi becerileriniz üst düzeyde. Kolektif zeka oluşturma ve çatışma dönüşümü konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> Kapsayıcı liderlik, çeşitlilik yönetimi ve ekip dinamikleri optimizasyonu konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi ekip liderliği rollerinde kullanarak, yüksek performanslı ekipler oluşturabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Ekip çalışması becerileriniz güçlü, çoğu durumda etkili işbirliği kurabiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Çatışma yönetimi ve uzaktan ekip çalışması konularında iyileştirme fırsatları var.</p><p><strong>Öneriler:</strong> Çatışma çözme teknikleri ve sanal ekip yönetimi becerileri geliştirerek etkinliğinizi artırabilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel ekip çalışması becerileriniz mevcut ancak daha etkili işbirliği ve çatışma yönetimi için gelişim gerekli.</p><p><strong>Gelişim Alanları:</strong> Ekip iletişimi, çatışma çözme ve çeşitlilik yönetimi konularında çalışma ihtiyacı var.</p><p><strong>Öneriler:</strong> Ekip çalışması eğitimleri alarak, işbirliği becerilerinizi geliştirin.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Ekip çalışması ve çatışma yönetimi becerilerinizin geliştirilmesi profesyonel başarınız için kritik önemde.</p><p><strong>Acil Gelişim Alanları:</strong> Temel işbirliği becerileri, iletişim ve çatışma önleme teknikleri.</p><p><strong>Öneriler:</strong> Temel ekip çalışması eğitimleri alarak, günlük işbirliği deneyimlerinizi iyileştirin.</p>"
                },
                "Öğrenme Çevikliği": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Öğrenme çevikliğiniz üst düzeyde. Hızlı adaptasyon, sürekli öğrenme ve bilgi transferi konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> Üst bilişsel stratejiler, deneysel öğrenme ve değişim çevikliği konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi inovasyon projelerinde kullanarak, organizasyonel öğrenme kapasitesini artırabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Öğrenme becerileriniz güçlü, yeni konulara hızlı adaptasyon sağlayabiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Belirsizlik toleransı ve teknoloji öğrenme hızı konularında iyileştirme fırsatları mevcut.</p><p><strong>Öneriler:</strong> Hızlandırılmış öğrenme teknikleri ve dijital akıcılık geliştirme yöntemleri öğrenebilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel öğrenme becerileriniz var ancak daha çevik ve etkili öğrenme stratejileri geliştirme ihtiyacınız bulunuyor.</p><p><strong>Gelişim Alanları:</strong> Öğrenme hızı, adaptasyon yeteneği ve bilgi uygulama konularında çalışma gerekli.</p><p><strong>Öneriler:</strong> Etkili öğrenme teknikleri eğitimleri alarak, öğrenme stratejilerinizi optimize edin.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Öğrenme çevikliğinizin geliştirilmesi değişen iş dünyasında başarılı olmanız için kritik öneme sahip.</p><p><strong>Acil Gelişim Alanları:</strong> Temel öğrenme becerileri, adaptasyon yeteneği ve sürekli gelişim zihniyeti.</p><p><strong>Öneriler:</strong> Temel öğrenme becerileri eğitimleri alarak, günlük öğrenme alışkanlıkları geliştirin.</p>"
                },
                "Duygusal Zeka ve Stres Toleransı": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Duygusal zeka ve stres toleransınız üst düzeyde. Duygusal düzenleme, empati ve dayanıklılık konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> İleri empati becerileri, stres-güç dönüşümü ve duygusal liderlik konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi liderlik ve mentorluk rollerinde kullanarak, pozitif çalışma ortamları oluşturabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Duygusal zeka becerileriniz güçlü, çoğu durumda etkili duygusal yönetim sergileyebiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Stres yönetimi ve olumsuz duygularla başa çıkma konularında iyileştirme fırsatları var.</p><p><strong>Öneriler:</strong> Dayanıklılık geliştirme teknikleri ve duygusal düzenleme stratejileri öğrenerek kendinizi geliştirebilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel duygusal zeka becerileriniz mevcut ancak daha etkili duygusal yönetim için gelişim gerekli.</p><p><strong>Gelişim Alanları:</strong> Öz farkındalık, empati kurma ve stres yönetimi konularında çalışma ihtiyacı var.</p><p><strong>Öneriler:</strong> Duygusal zeka eğitimleri alarak, günlük duygusal deneyimlerinizi iyileştirin.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Duygusal zeka ve stres toleransınızın geliştirilmesi kişisel refahınız ve profesyonel başarınız için kritik önemde.</p><p><strong>Acil Gelişim Alanları:</strong> Temel duygusal farkındalık, stres yönetimi ve empati becerileri.</p><p><strong>Öneriler:</strong> Duygusal zeka ve stres yönetimi eğitimleri alarak, temel becerileri geliştirmeye odaklanın.</p>"
                },
                "Profesyonel Marka ve Ağ Yönetimi": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Profesyonel marka ve ağ yönetimi becerileriniz üst düzeyde. Düşünce liderliği ve stratejik ilişki kurma konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> Kişisel marka stratejisi, dijital düşünce liderliği ve karşılıklı değer yaratma konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi sektör liderliği rollerinde kullanarak, geniş etki alanları oluşturabilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Profesyonel marka ve ağ oluşturma becerileriniz güçlü, etkili ilişkiler kurabiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Dijital varlık yönetimi ve sektör görünürlüğü konularında iyileştirme fırsatları mevcut.</p><p><strong>Öneriler:</strong> Dijital pazarlama teknikleri ve içerik stratejileri öğrenerek görünürlüğünüzü artırabilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel ağ oluşturma becerileriniz var ancak daha stratejik marka yönetimi için gelişim gerekli.</p><p><strong>Gelişim Alanları:</strong> Kişisel marka stratejisi, profesyonel ağ genişletme ve görünürlük artırma konularında çalışma ihtiyacı var.</p><p><strong>Öneriler:</strong> Kişisel marka geliştirme eğitimleri alarak, profesyonel varlığınızı güçlendirin.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Profesyonel marka ve ağ yönetiminizin geliştirilmesi kariyer ilerlemesi için kritik öneme sahip.</p><p><strong>Acil Gelişim Alanları:</strong> Temel ağ oluşturma becerileri, profesyonel iletişim ve marka farkındalığı.</p><p><strong>Öneriler:</strong> Temel ağ oluşturma eğitimleri alarak, profesyonel ilişki kurma becerilerinizi geliştirin.</p>"
                },
                "Yenilikçilik ve Geliştirme Odaklılık": {
                    excellent: "<p><strong>Mükemmel Seviye:</strong> Yenilikçilik ve geliştirme odaklılığınız üst düzeyde. Tasarım düşüncesi ve yıkıcı inovasyon konularında uzman seviyedesiniz.</p><p><strong>Güçlü Yönler:</strong> İnovasyon metodolojileri, gelecek öngörü ve ticarileştirme stratejileri konularında mükemmel yetkinlik.</p><p><strong>Öneriler:</strong> Bu yeteneklerinizi inovasyon liderliği rollerinde kullanarak, organizasyonel dönüşüm projelerine öncülük edebilirsiniz.</p>",
                    good: "<p><strong>İyi Seviye:</strong> Yenilikçilik becerileriniz güçlü, yaratıcı çözümler geliştirebiliyorsunuz.</p><p><strong>Gelişim Alanları:</strong> Risk alma stratejileri ve inovasyon proje yönetimi konularında iyileştirme fırsatları var.</p><p><strong>Öneriler:</strong> İnovasyon metodolojileri ve proje yönetimi teknikleri öğrenerek etkinliğinizi artırabilirsiniz.</p>",
                    average: "<p><strong>Orta Seviye:</strong> Temel yaratıcılık becerileriniz mevcut ancak daha sistematik inovasyon yaklaşımı geliştirme ihtiyacınız bulunuyor.</p><p><strong>Gelişim Alanları:</strong> Yaratıcı düşünme, trend analizi ve süreç iyileştirme konularında çalışma gerekli.</p><p><strong>Öneriler:</strong> Yaratıcılık ve inovasyon eğitimleri alarak, yenilikçi düşünce becerilerinizi geliştirin.</p>",
                    needs_improvement: "<p><strong>Gelişim Gereken Alan:</strong> Yenilikçilik ve geliştirme odaklılığınızın artırılması değişen iş dünyasında rekabet avantajı için kritik önemde.</p><p><strong>Acil Gelişim Alanları:</strong> Temel yaratıcılık becerileri, değişime açıklık ve sürekli iyileştirme zihniyeti.</p><p><strong>Öneriler:</strong> Temel yaratıcılık eğitimleri alarak, günlük çalışma rutinlerinizde yenilikçi yaklaşımlar deneyin.</p>"
                }
            };
            
            const categoryAnalysis = analyses[categoryName];
            if (!categoryAnalysis) return "<p>Bu kategori için analiz mevcut değil.</p>";
            
            if (percentage >= 85) return categoryAnalysis.excellent;
            if (percentage >= 70) return categoryAnalysis.good;
            if (percentage >= 55) return categoryAnalysis.average;
            return categoryAnalysis.needs_improvement;
        }

        // Global değişken tanımlaması
        let categoryScoresGlobal = [];

        // Türkçe karakter temizleme fonksiyonu (PDF için)
        function cleanTurkish(text) {
            if (!text) return '';
            // jsPDF'in helvetica fontu Türkçe karakterleri desteklemiyor
            // Bu yüzden en yakın ASCII karakterlere dönüştürüyoruz
            const map = {
                'ı': 'i', 'İ': 'I', 'ş': 's', 'Ş': 'S',
                'ğ': 'g', 'Ğ': 'G', 'ü': 'u', 'Ü': 'U',
                'ö': 'o', 'Ö': 'O', 'ç': 'c', 'Ç': 'C',
                'â': 'a', 'Â': 'A', 'î': 'i', 'Î': 'I',
                'û': 'u', 'Û': 'U'
            };
            return text.toString().replace(/[ıİşŞğĞüÜöÖçÇâÂîÎûÛ]/g, letter => map[letter] || letter);
        }

        // PDF Rapor Fonksiyonları
        async function downloadPDFReport() {
            if (!window.jspdf || !window.jspdf.jsPDF) {
                showMessage("PDF kütüphanesi yüklenemedi, lütfen sayfayı yenileyin.", "error");
                return;
            }

            showMessage("PDF hazırlanıyor, lütfen bekleyin...", "info");

            try {
                const { jsPDF } = window.jspdf;
                const doc = new jsPDF({
                    orientation: 'p',
                    unit: 'mm',
                    format: 'a4',
                    putOnlyUsedFonts: true,
                    compress: true,
                    floatPrecision: 16
                });
                
                doc.setLanguage("tr");
                
                const pageWidth = doc.internal.pageSize.getWidth();
                const pageHeight = doc.internal.pageSize.getHeight();
                let yPos = 20;

                // Türkçe karakter desteği için encoding ayarla
                doc.setCharSpace(0);

                // Başlık
                doc.setFillColor(102, 126, 234);
                doc.rect(0, 0, pageWidth, 40, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(24);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KARİYER GELİŞİM ENVANTERİ'), pageWidth / 2, 20, { align: 'center' });
                doc.setFontSize(12);
                doc.text(cleanTurkish('Profesyonel Yetkinlik Değerlendirme Raporu'), pageWidth / 2, 30, { align: 'center' });

                yPos = 50;

                // Katılımcı Bilgileri
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(10);
                const reportDate = new Date().toLocaleDateString('tr-TR', { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit'
                });
                
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Katılımcı:'), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.nickname), 50, yPos);
                yPos += 7;

                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Rapor Tarihi:'), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(reportDate), 50, yPos);
                yPos += 7;

                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Mezuniyet:'), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.education_level), 50, yPos);
                yPos += 7;

                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Bölüm:'), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.department), 50, yPos);
                yPos += 7;

                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Pozisyon:'), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.current_position), 50, yPos);
                yPos += 12;

                // Genel Skor
                const overallScore = document.getElementById('overallScore').textContent;
                doc.setFillColor(102, 126, 234);
                doc.roundedRect(15, yPos, pageWidth - 30, 20, 3, 3, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(16);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('GENEL SKOR: ') + overallScore, pageWidth / 2, yPos + 12, { align: 'center' });
                yPos += 30;

                // Açıklama metni
                doc.setTextColor(80, 80, 80);
                doc.setFontSize(9);
                doc.setFont('helvetica', 'italic');
                const infoText1 = cleanTurkish('Kariyer Gelişim Çerçevesi (KGC), gençlerin öz-farkındalık, potansiyel keşfi ve düşünce yapısını tetikleme amacıyla tasarlanmış profesyonel bir araçtır. Test sonuçları, bir profesyonel kariyer planının veya tıbbi/psikolojik bir tanının yerini tutmaz.');
                const splitInfo1 = doc.splitTextToSize(infoText1, pageWidth - 40);
                doc.text(splitInfo1, 20, yPos);
                yPos += splitInfo1.length * 4 + 4;
                
                const infoText2 = cleanTurkish('Kullanıcı, test sonuçlarına dayanarak tek başına herhangi bir kesin kariyer kararı veya aksiyon planı belirlememelidir. Test sonuçlarının hatalı veya eksik yorumlanması, kullanıcı için uygun olmayan kararlara ve dolayısıyla hatalı sonuçlara yol açabilir.');
                const splitInfo2 = doc.splitTextToSize(infoText2, pageWidth - 40);
                doc.text(splitInfo2, 20, yPos);
                yPos += splitInfo2.length * 4 + 4;
                
                const infoText3 = cleanTurkish('Kullanıcının, KGC sonuçlarını kariyer yolculuğuna entegre etmesi ve bu sonuçlara dayanarak anlamlı, sağlam adımlar atması için mutlaka lisanslı ve/veya yetkili bir profesyonel danışmanlık hizmeti alması şiddetle tavsiye edilir.');
                const splitInfo3 = doc.splitTextToSize(infoText3, pageWidth - 40);
                doc.text(splitInfo3, 20, yPos);
                yPos += splitInfo3.length * 4 + 10;

                // Kategori Sonuçları
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KATEGORİ SONUÇLARI'), 15, yPos);
                yPos += 10;

                if (!window.categoryScoresGlobal || window.categoryScoresGlobal.length === 0) {
                    showMessage("Kategori sonuçları bulunamadı!", "error");
                    return;
                }

                window.categoryScoresGlobal.forEach((category, index) => {
                    if (yPos > pageHeight - 30) {
                        doc.addPage();
                        yPos = 20;
                    }

                    // Numara ve kategori adı
                    doc.setFontSize(10);
                    doc.setFont('helvetica', 'bold');
                    doc.setTextColor(102, 126, 234);
                    doc.text((index + 1).toString(), 15, yPos);
                    
                    doc.setTextColor(0, 0, 0);
                    doc.text(cleanTurkish(category.name), 22, yPos);
                    yPos += 5;
                    
                    // Skor detayı
                    const scoreText = Math.round(category.percentage) + '% - ' + category.score + '/40';
                    doc.setFontSize(9);
                    doc.setFont('helvetica', 'normal');
                    doc.setTextColor(100, 100, 100);
                    doc.text(scoreText, 22, yPos);
                    yPos += 3;

                    // Progress bar
                    doc.setDrawColor(220, 220, 220);
                    doc.setLineWidth(0.3);
                    doc.rect(22, yPos, pageWidth - 37, 4);
                    
                    const barWidth = ((pageWidth - 37) * category.percentage) / 100;
                    doc.setFillColor(102, 126, 234);
                    doc.rect(22, yPos, barWidth, 4, 'F');
                    yPos += 10;
                });

                // Yorum ekle
                yPos += 5;
                if (yPos > pageHeight - 50) {
                    doc.addPage();
                    yPos = 20;
                }

                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('DEĞERLENDİRME'), 15, yPos);
                yPos += 8;

                doc.setFontSize(10);
                doc.setFont('helvetica', 'normal');
                const interpretation = document.getElementById('scoreInterpretation').textContent;
                const splitInterpretation = doc.splitTextToSize(cleanTurkish(interpretation), pageWidth - 30);
                doc.text(splitInterpretation, 15, yPos);
                yPos += splitInterpretation.length * 5 + 10;

                // Uyarı
                if (yPos > pageHeight - 40) {
                    doc.addPage();
                    yPos = 20;
                }

                doc.setFillColor(255, 243, 205);
                doc.roundedRect(15, yPos, pageWidth - 30, 35, 3, 3, 'F');
                doc.setFontSize(10);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(133, 100, 4);
                doc.text(cleanTurkish('ÖNEMLİ UYARI'), 20, yPos + 8);
                doc.setFont('helvetica', 'normal');
                const warningText = cleanTurkish('Bu analizin yorumlanması için mutlaka profesyonel bir destek ve danışmanlık alınız. Bu rapor üzerinden yaptığınız bireysel çıkarımlar sizi hatalı değerlendirmelere sevk edebilir.');
                const splitWarning = doc.splitTextToSize(warningText, pageWidth - 40);
                doc.text(splitWarning, 20, yPos + 15);

                // Footer
                doc.setTextColor(150, 150, 150);
                doc.setFontSize(8);
                doc.text(cleanTurkish('© 2025 Kariyer Gelişim Envanteri - AKÇA PRO X ANALİZİ'), pageWidth / 2, pageHeight - 10, { align: 'center' });

                // PDF'i kaydet
                const fileName = `Kariyer_Raporu_${cleanTurkish(currentUser.nickname)}_${new Date().toISOString().split('T')[0]}.pdf`;
                doc.save(fileName);
                showMessage("PDF rapor başarıyla indirildi!", "success");

            } catch (error) {
                console.error('PDF oluşturma hatası:', error);
                showMessage("PDF oluşturulurken hata oluştu: " + error.message, "error");
            }
        }

        async function downloadDetailedPDFReport() {
            if (!window.jspdf || !window.jspdf.jsPDF || !window.html2canvas) {
                showMessage("PDF kütüphaneleri yüklenemedi, lütfen sayfayı yenileyin.", "error");
                return;
            }

            showMessage("Detaylı PDF hazırlanıyor, bu biraz zaman alabilir...", "info");

            try {
                const { jsPDF } = window.jspdf;
                const doc = new jsPDF({
                    orientation: 'p',
                    unit: 'mm',
                    format: 'a4',
                    putOnlyUsedFonts: true,
                    compress: true,
                    floatPrecision: 16
                });
                
                doc.setLanguage("tr");
                
                const pageWidth = doc.internal.pageSize.getWidth();
                const pageHeight = doc.internal.pageSize.getHeight();
                let yPos = 20;

                // Türkçe karakter desteği için encoding ayarla
                doc.setCharSpace(0);

                // Başlık
                doc.setFillColor(102, 126, 234);
                doc.rect(0, 0, pageWidth, 45, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(22);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('AKÇA PRO X ANALİZİ'), pageWidth / 2, 18, { align: 'center' });
                doc.setFontSize(16);
                doc.text(cleanTurkish('Detaylı Kariyer Yetkinlik Analizi'), pageWidth / 2, 28, { align: 'center' });
                doc.setFontSize(10);
                doc.setFont('helvetica', 'normal');
                const reportDate = new Date().toLocaleDateString('tr-TR', { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit'
                });
                doc.text(cleanTurkish('Rapor Tarihi: ') + cleanTurkish(reportDate), pageWidth / 2, 38, { align: 'center' });

                yPos = 55;

                // Katılımcı Bilgileri
                doc.setTextColor(0, 0, 0);
                doc.setFillColor(248, 249, 250);
                doc.roundedRect(15, yPos, pageWidth - 30, 35, 3, 3, 'F');
                yPos += 8;

                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KATILIMCI BİLGİLERİ'), 20, yPos);
                yPos += 7;

                doc.setFontSize(10);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish('Rumuz: ') + cleanTurkish(currentUser.nickname), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish('Mezuniyet: ') + cleanTurkish(currentUser.education_level), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish('Bölüm: ') + cleanTurkish(currentUser.department), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish('Pozisyon: ') + cleanTurkish(currentUser.current_position), 20, yPos);
                yPos += 12;

                // Genel Skor
                const overallScore = document.getElementById('reportOverallScore').textContent;
                doc.setFillColor(102, 126, 234);
                doc.roundedRect(15, yPos, pageWidth - 30, 25, 3, 3, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(20);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('GENEL SKOR: ') + overallScore, pageWidth / 2, yPos + 16, { align: 'center' });
                yPos += 35;

                // Açıklama metni
                doc.setTextColor(80, 80, 80);
                doc.setFontSize(9);
                doc.setFont('helvetica', 'italic');
                const infoText1 = cleanTurkish('Kariyer Gelişim Çerçevesi (KGC), gençlerin öz-farkındalık, potansiyel keşfi ve düşünce yapısını tetikleme amacıyla tasarlanmış profesyonel bir araçtır. Test sonuçları, bir profesyonel kariyer planının veya tıbbi/psikolojik bir tanının yerini tutmaz.');
                const splitInfo1 = doc.splitTextToSize(infoText1, pageWidth - 40);
                doc.text(splitInfo1, 20, yPos);
                yPos += splitInfo1.length * 4 + 4;
                
                const infoText2 = cleanTurkish('Kullanıcı, test sonuçlarına dayanarak tek başına herhangi bir kesin kariyer kararı veya aksiyon planı belirlememelidir. Test sonuçlarının hatalı veya eksik yorumlanması, kullanıcı için uygun olmayan kararlara ve dolayısıyla hatalı sonuçlara yol açabilir.');
                const splitInfo2 = doc.splitTextToSize(infoText2, pageWidth - 40);
                doc.text(splitInfo2, 20, yPos);
                yPos += splitInfo2.length * 4 + 4;
                
                const infoText3 = cleanTurkish('Kullanıcının, KGC sonuçlarını kariyer yolculuğuna entegre etmesi ve bu sonuçlara dayanarak anlamlı, sağlam adımlar atması için mutlaka lisanslı ve/veya yetkili bir profesyonel danışmanlık hizmeti alması şiddetle tavsiye edilir.');
                const splitInfo3 = doc.splitTextToSize(infoText3, pageWidth - 40);
                doc.text(splitInfo3, 20, yPos);
                yPos += splitInfo3.length * 4 + 15;

                // Kategori Sonuçları Listesi
                doc.addPage();
                yPos = 20;
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KATEGORİ SONUÇLARI'), pageWidth / 2, yPos, { align: 'center' });
                yPos += 10;

                window.categoryScoresGlobal.forEach((category, index) => {
                    if (yPos > pageHeight - 30) {
                        doc.addPage();
                        yPos = 20;
                    }

                    // Numara ve kategori adı
                    doc.setFontSize(10);
                    doc.setFont('helvetica', 'bold');
                    doc.setTextColor(102, 126, 234);
                    doc.text((index + 1).toString(), 15, yPos);
                    
                    doc.setTextColor(0, 0, 0);
                    doc.text(cleanTurkish(category.name), 22, yPos);
                    yPos += 5;
                    
                    // Skor detayı
                    const scoreText = Math.round(category.percentage) + '% - ' + category.score + '/40';
                    doc.setFontSize(9);
                    doc.setFont('helvetica', 'normal');
                    doc.setTextColor(100, 100, 100);
                    doc.text(scoreText, 22, yPos);
                    yPos += 3;

                    // Progress bar
                    doc.setDrawColor(220, 220, 220);
                    doc.setLineWidth(0.3);
                    doc.rect(22, yPos, pageWidth - 37, 4);
                    
                    const barWidth = ((pageWidth - 37) * category.percentage) / 100;
                    doc.setFillColor(102, 126, 234);
                    doc.rect(22, yPos, barWidth, 4, 'F');
                    yPos += 10;
                });

                // Grafikleri ekle
                doc.addPage();
                yPos = 20;
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('GRAFİK ANALİZLER'), pageWidth / 2, yPos, { align: 'center' });
                yPos += 10;

                // Grafikleri canvas'tan al ve PDF'e ekle
                const charts = ['radarChart', 'pieChart', 'barChart', 'scatterChart'];
                const chartTitles = [
                    cleanTurkish('Radar Analizi'), 
                    cleanTurkish('Pasta Grafiği'), 
                    cleanTurkish('Çubuk Grafiği'), 
                    cleanTurkish('Nokta Grafiği')
                ];
                
                for (let i = 0; i < charts.length; i++) {
                    const canvas = document.getElementById(charts[i]);
                    if (canvas) {
                        const imgData = canvas.toDataURL('image/png');
                        const imgWidth = 80;
                        const imgHeight = 80;
                        const xPos = (i % 2 === 0) ? 15 : pageWidth / 2 + 5;
                        const currentYPos = yPos + Math.floor(i / 2) * 90;

                        if (currentYPos + imgHeight > pageHeight - 20) {
                            doc.addPage();
                            yPos = 20;
                        }

                        doc.setFontSize(11);
                        doc.setFont('helvetica', 'bold');
                        doc.text(chartTitles[i], xPos + imgWidth / 2, currentYPos, { align: 'center' });
                        doc.addImage(imgData, 'PNG', xPos, currentYPos + 5, imgWidth, imgHeight);
                    }
                }

                // Grafik açıklamaları - Yeni sayfa
                doc.addPage();
                yPos = 20;
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(0, 0, 0);
                doc.text(cleanTurkish('GRAFİK AÇIKLAMALARI'), pageWidth / 2, yPos, { align: 'center' });
                yPos += 10;

                // Pasta grafiği açıklamaları
                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Pasta Grafiği Dağılımı'), 15, yPos);
                yPos += 7;

                doc.setFontSize(9);
                doc.setFont('helvetica', 'normal');
                const totalScore = window.categoryScoresGlobal.reduce((sum, cat) => sum + cat.score, 0);
                
                window.categoryScoresGlobal.forEach((category, index) => {
                    if (yPos > pageHeight - 15) {
                        doc.addPage();
                        yPos = 20;
                    }

                    const pieShare = Math.round((category.score / totalScore) * 100);
                    const categoryText = `${index + 1}. ${cleanTurkish(category.name)}`;
                    const scoreInfo = cleanTurkish(`Pasta Payi: ${pieShare}% | Skor: ${category.score}/40 (${Math.round(category.percentage)}%)`);
                    
                    doc.setFont('helvetica', 'bold');
                    doc.text(categoryText, 15, yPos);
                    yPos += 4;
                    doc.setFont('helvetica', 'normal');
                    doc.setTextColor(100, 100, 100);
                    doc.text(scoreInfo, 15, yPos);
                    doc.setTextColor(0, 0, 0);
                    yPos += 7;
                });

                // Radar, Çubuk ve Nokta Grafikleri için ortak açıklama
                yPos += 5;
                if (yPos > pageHeight - 80) {
                    doc.addPage();
                    yPos = 20;
                }

                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Radar / Çubuk / Nokta Grafikleri Kategori Listesi'), 15, yPos);
                yPos += 7;

                doc.setFontSize(9);
                doc.setFont('helvetica', 'normal');
                
                window.categoryScoresGlobal.forEach((category, index) => {
                    if (yPos > pageHeight - 15) {
                        doc.addPage();
                        yPos = 20;
                    }

                    const categoryText = `${index + 1}. ${cleanTurkish(category.name)}`;
                    const scoreInfo = cleanTurkish(`Skor: ${category.score}/40 (${Math.round(category.percentage)}%)`);
                    
                    doc.setFont('helvetica', 'bold');
                    doc.text(categoryText, 15, yPos);
                    yPos += 4;
                    doc.setFont('helvetica', 'normal');
                    doc.setTextColor(100, 100, 100);
                    doc.text(scoreInfo, 15, yPos);
                    doc.setTextColor(0, 0, 0);
                    yPos += 7;
                });

                // Kategori analizleri
                doc.addPage();
                yPos = 20;
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KATEGORİ ANALİZLERİ'), pageWidth / 2, yPos, { align: 'center' });
                yPos += 10;

                window.categoryScoresGlobal.forEach((category, index) => {
                    if (yPos > pageHeight - 60) {
                        doc.addPage();
                        yPos = 20;
                    }

                    // Kategori başlığı
                    doc.setFillColor(240, 244, 255);
                    doc.roundedRect(15, yPos, pageWidth - 30, 10, 2, 2, 'F');
                    doc.setFontSize(11);
                    doc.setFont('helvetica', 'bold');
                    doc.setTextColor(102, 126, 234);
                    doc.text(cleanTurkish(category.name), 20, yPos + 7);
                    
                    // Skor badge
                    const scoreText = Math.round(category.percentage) + '%';
                    doc.text(scoreText, pageWidth - 20, yPos + 7, { align: 'right' });
                    yPos += 15;

                    // Analiz metni
                    doc.setTextColor(0, 0, 0);
                    doc.setFontSize(9);
                    doc.setFont('helvetica', 'normal');
                    const analysis = getCategoryAnalysis(category.name, category.percentage);
                    
                    // HTML etiketlerini temizle ve Türkçe karakterleri dönüştür
                    const tempDiv = document.createElement('div');
                    tempDiv.innerHTML = analysis;
                    const cleanText = cleanTurkish(tempDiv.textContent || tempDiv.innerText || '');
                    
                    const lines = doc.splitTextToSize(cleanText, pageWidth - 40);
                    lines.forEach((line, lineIndex) => {
                        if (yPos > pageHeight - 15) {
                            doc.addPage();
                            yPos = 20;
                        }
                        doc.text(line, 20, yPos);
                        yPos += 5;
                    });
                    yPos += 8;
                });

                // Genel Değerlendirme
                if (yPos > pageHeight - 50) {
                    doc.addPage();
                    yPos = 20;
                } else {
                    yPos += 10;
                }

                doc.setFillColor(240, 244, 255);
                doc.roundedRect(15, yPos, pageWidth - 30, 8, 2, 2, 'F');
                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(102, 126, 234);
                doc.text(cleanTurkish('GENEL DEĞERLENDİRME'), 20, yPos + 6);
                yPos += 14;

                doc.setTextColor(0, 0, 0);
                doc.setFontSize(10);
                doc.setFont('helvetica', 'normal');
                
                // Puana göre yorum oluştur
                const currentScore = parseFloat(overallScore);
                let generalInterpretation = '';
                if (currentScore >= 85) {
                    generalInterpretation = 'Mükemmel! Kariyer gelişiminizde çok güçlü bir konumdasınız.';
                } else if (currentScore >= 70) {
                    generalInterpretation = 'Çok iyi! Güçlü yönleriniz var, bazı alanlarda gelişim fırsatları mevcut.';
                } else if (currentScore >= 60) {
                    generalInterpretation = 'İyi seviyede! Belirli alanlarda odaklanarak daha da güçlenebilirsiniz.';
                } else if (currentScore >= 45) {
                    generalInterpretation = 'Orta seviyede. Gelişim için net yol haritası belirlenebilir.';
                } else {
                    generalInterpretation = 'Gelişim potansiyeli yüksek! Sistematik çalışmayla büyük ilerleme kaydedebilirsiniz.';
                }
                
                const splitGeneral = doc.splitTextToSize(cleanTurkish(generalInterpretation), pageWidth - 40);
                doc.text(splitGeneral, 20, yPos);
                yPos += splitGeneral.length * 6 + 10;

                // Uyarı sayfası
                doc.addPage();
                yPos = 40;
                doc.setFillColor(255, 243, 205);
                doc.roundedRect(15, yPos, pageWidth - 30, 60, 5, 5, 'F');
                
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(220, 53, 69);
                doc.text(cleanTurkish('ÖNEMLİ UYARI'), pageWidth / 2, yPos + 12, { align: 'center' });
                
                yPos += 22;
                doc.setFontSize(10);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(133, 100, 4);
                const warningTitle = cleanTurkish('Bu analizin yorumlanması için mutlaka profesyonel bir destek ve danışmanlık alınız.');
                const splitTitle = doc.splitTextToSize(warningTitle, pageWidth - 50);
                doc.text(splitTitle, pageWidth / 2, yPos, { align: 'center' });
                
                yPos += splitTitle.length * 5 + 5;
                doc.setFont('helvetica', 'normal');
                const warningText = cleanTurkish('Bu rapor üzerinden yaptığınız bireysel çıkarımlar sizi hatalı değerlendirmelere sevk edebilir. Sonuçlar genel bir değerlendirme niteliğindedir ve profesyonel kariyer danışmanlığının yerini tutmaz.');
                const splitWarning = doc.splitTextToSize(warningText, pageWidth - 50);
                doc.text(splitWarning, pageWidth / 2, yPos, { align: 'center' });

                // Footer - tüm sayfalara
                const totalPages = doc.internal.getNumberOfPages();
                for (let i = 1; i <= totalPages; i++) {
                    doc.setPage(i);
                    doc.setTextColor(150, 150, 150);
                    doc.setFontSize(8);
                    doc.text(cleanTurkish('Sayfa ') + i + ' / ' + totalPages, pageWidth / 2, pageHeight - 10, { align: 'center' });
                    doc.text(cleanTurkish('© 2025 Kariyer Gelişim Envanteri - AKÇA PRO X ANALİZİ'), pageWidth / 2, pageHeight - 5, { align: 'center' });
                }

                // PDF'i kaydet
                const fileName = `Detayli_Kariyer_Raporu_${cleanTurkish(currentUser.nickname)}_${new Date().toISOString().split('T')[0]}.pdf`;
                doc.save(fileName);
                showMessage("Detaylı PDF rapor başarıyla indirildi!", "success");

            } catch (error) {
                console.error('Detaylı PDF oluşturma hatası:', error);
                showMessage("PDF oluşturulurken hata oluştu: " + error.message, "error");
            }
        }

        // Ortalama Rapor PDF'i
        async function downloadAveragePDFReport() {
            try {
                if (!currentUser || !currentUser.test_history || currentUser.test_history.length === 0) {
                    showMessage("PDF oluşturmak için test geçmişi bulunamadı!", "error");
                    return;
                }

                const { jsPDF } = window.jspdf;
                const doc = new jsPDF();
                const pageWidth = doc.internal.pageSize.getWidth();
                const pageHeight = doc.internal.pageSize.getHeight();

                // Ortalama skorları hesapla
                const categoryAverages = {};
                currentUser.test_history.forEach(test => {
                    const results = JSON.parse(test.test_results);
                    results.forEach(category => {
                        if (!categoryAverages[category.name]) {
                            categoryAverages[category.name] = { name: category.name, totalScore: 0, totalPercentage: 0, count: 0 };
                        }
                        categoryAverages[category.name].totalScore += category.score;
                        categoryAverages[category.name].totalPercentage += category.percentage;
                        categoryAverages[category.name].count++;
                    });
                });

                const avgCategoryScores = Object.values(categoryAverages).map(cat => ({
                    name: cat.name,
                    score: Math.round(cat.totalScore / cat.count),
                    percentage: cat.totalPercentage / cat.count
                }));

                const avgOverallScore = Math.round(
                    currentUser.test_history.reduce((sum, test) => sum + test.overall_score, 0) / 
                    currentUser.test_history.length
                );

                // Başlık
                doc.setFillColor(102, 126, 234);
                doc.rect(0, 0, pageWidth, 40, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(20);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('ORTALAMA KARİYER GELİŞİM RAPORU'), pageWidth / 2, 15, { align: 'center' });
                doc.setFontSize(12);
                doc.text(cleanTurkish('AKÇA PRO X ANALİZİ'), pageWidth / 2, 25, { align: 'center' });
                doc.setFontSize(10);
                doc.text(cleanTurkish(`${currentUser.test_history.length} Test Ortalaması`), pageWidth / 2, 33, { align: 'center' });

                // Kullanıcı bilgileri
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(10);
                let yPos = 50;
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Kullanıcı: '), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.nickname), 45, yPos);
                yPos += 8;
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Rapor Tarihi: '), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(new Date().toLocaleDateString('tr-TR'), 45, yPos);

                // Genel Skor
                yPos += 15;
                doc.setFillColor(240, 244, 255);
                doc.roundedRect(15, yPos, pageWidth - 30, 25, 5, 5, 'F');
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(102, 126, 234);
                doc.text(cleanTurkish('ORTALAMA GENEL SKOR: ') + avgOverallScore + '%', pageWidth / 2, yPos + 16, { align: 'center' });

                // Kategori ortalamaları
                yPos += 35;
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KATEGORİ ORTALAMALARI'), 15, yPos);
                yPos += 8;

                doc.setFontSize(9);
                avgCategoryScores.forEach((category, index) => {
                    if (yPos > pageHeight - 20) {
                        doc.addPage();
                        yPos = 20;
                    }

                    doc.setFont('helvetica', 'bold');
                    doc.text(`${index + 1}. ${cleanTurkish(category.name)}`, 15, yPos);
                    yPos += 4;
                    doc.setFont('helvetica', 'normal');
                    doc.setTextColor(100, 100, 100);
                    doc.text(cleanTurkish(`Ortalama Skor: ${category.score}/40 (${Math.round(category.percentage)}%)`), 15, yPos);
                    doc.setTextColor(0, 0, 0);
                    yPos += 7;
                });

                // Footer
                const totalPages = doc.internal.getNumberOfPages();
                for (let i = 1; i <= totalPages; i++) {
                    doc.setPage(i);
                    doc.setTextColor(150, 150, 150);
                    doc.setFontSize(8);
                    doc.text(cleanTurkish('Sayfa ') + i + ' / ' + totalPages, pageWidth / 2, pageHeight - 10, { align: 'center' });
                    doc.text(cleanTurkish('© 2025 Ortalama Kariyer Raporu - AKÇA PRO X'), pageWidth / 2, pageHeight - 5, { align: 'center' });
                }

                const fileName = `Ortalama_Kariyer_Raporu_${cleanTurkish(currentUser.nickname)}_${new Date().toISOString().split('T')[0]}.pdf`;
                doc.save(fileName);
                showMessage("Ortalama rapor PDF'i başarıyla indirildi!", "success");

            } catch (error) {
                console.error('Ortalama PDF oluşturma hatası:', error);
                showMessage("PDF oluşturulurken hata oluştu: " + error.message, "error");
            }
        }

        // İlerleme Grafiği PDF'i
        async function downloadProgressPDFReport() {
            try {
                if (!currentUser || !currentUser.test_history || currentUser.test_history.length === 0) {
                    showMessage("PDF oluşturmak için test geçmişi bulunamadı!", "error");
                    return;
                }

                const { jsPDF } = window.jspdf;
                const doc = new jsPDF();
                const pageWidth = doc.internal.pageSize.getWidth();
                const pageHeight = doc.internal.pageSize.getHeight();

                const sortedHistory = [...currentUser.test_history].sort((a, b) => 
                    new Date(a.test_date) - new Date(b.test_date)
                );

                // Başlık
                doc.setFillColor(102, 126, 234);
                doc.rect(0, 0, pageWidth, 40, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(20);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KARİYER GELİŞİM İLERLEME GRAFİĞİ'), pageWidth / 2, 15, { align: 'center' });
                doc.setFontSize(12);
                doc.text(cleanTurkish('AKÇA PRO X ANALİZİ'), pageWidth / 2, 25, { align: 'center' });
                doc.setFontSize(10);
                doc.text(cleanTurkish(`${sortedHistory.length} Test Sonucu`), pageWidth / 2, 33, { align: 'center' });

                // Kullanıcı bilgileri
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(10);
                let yPos = 50;
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Kullanıcı: '), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.nickname), 45, yPos);
                yPos += 8;
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Rapor Tarihi: '), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(new Date().toLocaleDateString('tr-TR'), 45, yPos);

                // Test detayları tablosu
                yPos += 15;
                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('TEST DETAYLARI'), 15, yPos);
                yPos += 8;

                // Tablo başlıkları
                doc.setFillColor(240, 244, 255);
                doc.rect(15, yPos, pageWidth - 30, 8, 'F');
                doc.setFontSize(9);
                doc.setFont('helvetica', 'bold');
                doc.text('#', 20, yPos + 6);
                doc.text(cleanTurkish('Tarih'), 35, yPos + 6);
                doc.text(cleanTurkish('Skor'), 90, yPos + 6);
                doc.text(cleanTurkish('Değişim'), 120, yPos + 6);
                yPos += 10;

                // Test satırları
                doc.setFont('helvetica', 'normal');
                sortedHistory.forEach((test, index) => {
                    if (yPos > pageHeight - 20) {
                        doc.addPage();
                        yPos = 20;
                    }

                    const testDate = new Date(test.test_date).toLocaleDateString('tr-TR', { 
                        year: 'numeric', 
                        month: 'short', 
                        day: 'numeric'
                    });

                    let change = '-';
                    if (index > 0) {
                        const diff = test.overall_score - sortedHistory[index - 1].overall_score;
                        if (diff > 0) {
                            change = `+${diff}%`;
                        } else if (diff < 0) {
                            change = `${diff}%`;
                        } else {
                            change = '0%';
                        }
                    }

                    doc.text(`${index + 1}`, 20, yPos);
                    doc.text(cleanTurkish(testDate), 35, yPos);
                    doc.text(`${test.overall_score}%`, 90, yPos);
                    doc.text(cleanTurkish(change), 120, yPos);
                    yPos += 6;
                });

                // İstatistikler
                yPos += 10;
                if (yPos > pageHeight - 40) {
                    doc.addPage();
                    yPos = 20;
                }

                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('İSTATİSTİKLER'), 15, yPos);
                yPos += 8;

                const scores = sortedHistory.map(t => t.overall_score);
                const minScore = Math.min(...scores);
                const maxScore = Math.max(...scores);
                const avgScore = Math.round(scores.reduce((a, b) => a + b, 0) / scores.length);
                const firstScore = scores[0];
                const lastScore = scores[scores.length - 1];
                const totalChange = lastScore - firstScore;

                doc.setFontSize(10);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(`En Düşük Skor: ${minScore}%`), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish(`En Yüksek Skor: ${maxScore}%`), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish(`Ortalama Skor: ${avgScore}%`), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish(`İlk Test Skoru: ${firstScore}%`), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish(`Son Test Skoru: ${lastScore}%`), 20, yPos);
                yPos += 6;
                doc.text(cleanTurkish(`Toplam Değişim: ${totalChange >= 0 ? '+' : ''}${totalChange}%`), 20, yPos);

                // Footer
                const totalPages = doc.internal.getNumberOfPages();
                for (let i = 1; i <= totalPages; i++) {
                    doc.setPage(i);
                    doc.setTextColor(150, 150, 150);
                    doc.setFontSize(8);
                    doc.text(cleanTurkish('Sayfa ') + i + ' / ' + totalPages, pageWidth / 2, pageHeight - 10, { align: 'center' });
                    doc.text(cleanTurkish('© 2025 İlerleme Raporu - AKÇA PRO X'), pageWidth / 2, pageHeight - 5, { align: 'center' });
                }

                const fileName = `Ilerleme_Raporu_${cleanTurkish(currentUser.nickname)}_${new Date().toISOString().split('T')[0]}.pdf`;
                doc.save(fileName);
                showMessage("İlerleme raporu PDF'i başarıyla indirildi!", "success");

            } catch (error) {
                console.error('İlerleme PDF oluşturma hatası:', error);
                showMessage("PDF oluşturulurken hata oluştu: " + error.message, "error");
            }
        }

        // Karşılaştırma Rapor PDF'i
        async function downloadComparisonPDFReport(oldIndex, newIndex) {
            try {
                if (!currentUser || !currentUser.test_history) {
                    showMessage("PDF oluşturmak için test geçmişi bulunamadı!", "error");
                    return;
                }

                const sortedHistory = [...currentUser.test_history].sort((a, b) => 
                    new Date(b.test_date) - new Date(a.test_date)
                );

                const oldTest = sortedHistory[oldIndex];
                const newTest = sortedHistory[newIndex];
                const oldResults = JSON.parse(oldTest.test_results);
                const newResults = JSON.parse(newTest.test_results);

                const { jsPDF } = window.jspdf;
                const doc = new jsPDF();
                const pageWidth = doc.internal.pageSize.getWidth();
                const pageHeight = doc.internal.pageSize.getHeight();

                const oldDate = new Date(oldTest.test_date).toLocaleDateString('tr-TR');
                const newDate = new Date(newTest.test_date).toLocaleDateString('tr-TR');

                // Başlık
                doc.setFillColor(102, 126, 234);
                doc.rect(0, 0, pageWidth, 40, 'F');
                doc.setTextColor(255, 255, 255);
                doc.setFontSize(20);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('TEST KARŞILAŞTIRMA RAPORU'), pageWidth / 2, 15, { align: 'center' });
                doc.setFontSize(12);
                doc.text(cleanTurkish('AKÇA PRO X ANALİZİ'), pageWidth / 2, 25, { align: 'center' });
                doc.setFontSize(10);
                doc.text(cleanTurkish(`${oldDate} vs ${newDate}`), pageWidth / 2, 33, { align: 'center' });

                // Kullanıcı bilgileri
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(10);
                let yPos = 50;
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Kullanıcı: '), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(cleanTurkish(currentUser.nickname), 45, yPos);
                yPos += 8;
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('Rapor Tarihi: '), 15, yPos);
                doc.setFont('helvetica', 'normal');
                doc.text(new Date().toLocaleDateString('tr-TR'), 45, yPos);

                // Genel Skor Karşılaştırması
                yPos += 15;
                doc.setFillColor(240, 244, 255);
                doc.roundedRect(15, yPos, pageWidth - 30, 30, 5, 5, 'F');
                doc.setFontSize(14);
                doc.setFont('helvetica', 'bold');
                doc.setTextColor(102, 126, 234);
                doc.text(cleanTurkish('GENEL SKOR DEĞİŞİMİ'), pageWidth / 2, yPos + 10, { align: 'center' });
                doc.setTextColor(0, 0, 0);
                doc.setFontSize(12);
                const scoreDiff = newTest.overall_score - oldTest.overall_score;
                const scoreText = cleanTurkish(`${oldTest.overall_score}% → ${newTest.overall_score}% (${scoreDiff >= 0 ? '+' : ''}${scoreDiff}%)`);
                doc.text(scoreText, pageWidth / 2, yPos + 22, { align: 'center' });

                // Kategori Karşılaştırmaları
                yPos += 40;
                doc.setFontSize(12);
                doc.setFont('helvetica', 'bold');
                doc.text(cleanTurkish('KATEGORİ KARŞILAŞTIRMALARI'), 15, yPos);
                yPos += 8;

                doc.setFontSize(9);
                oldResults.forEach((oldCat, index) => {
                    if (yPos > pageHeight - 25) {
                        doc.addPage();
                        yPos = 20;
                    }

                    const newCat = newResults[index];
                    const change = newCat.percentage - oldCat.percentage;

                    doc.setFont('helvetica', 'bold');
                    doc.text(`${index + 1}. ${cleanTurkish(oldCat.name)}`, 15, yPos);
                    yPos += 4;
                    doc.setFont('helvetica', 'normal');
                    doc.setTextColor(100, 100, 100);
                    doc.text(cleanTurkish(`Eski: ${Math.round(oldCat.percentage)}% | Yeni: ${Math.round(newCat.percentage)}% | Fark: ${change >= 0 ? '+' : ''}${Math.round(change)}%`), 15, yPos);
                    doc.setTextColor(0, 0, 0);
                    yPos += 7;
                });

                // Footer
                const totalPages = doc.internal.getNumberOfPages();
                for (let i = 1; i <= totalPages; i++) {
                    doc.setPage(i);
                    doc.setTextColor(150, 150, 150);
                    doc.setFontSize(8);
                    doc.text(cleanTurkish('Sayfa ') + i + ' / ' + totalPages, pageWidth / 2, pageHeight - 10, { align: 'center' });
                    doc.text(cleanTurkish('© 2025 Karşılaştırma Raporu - AKÇA PRO X'), pageWidth / 2, pageHeight - 5, { align: 'center' });
                }

                const fileName = `Karsilastirma_Raporu_${cleanTurkish(currentUser.nickname)}_${new Date().toISOString().split('T')[0]}.pdf`;
                doc.save(fileName);
                showMessage("Karşılaştırma raporu PDF'i başarıyla indirildi!", "success");

            } catch (error) {
                console.error('Karşılaştırma PDF oluşturma hatası:', error);
                showMessage("PDF oluşturulurken hata oluştu: " + error.message, "error");
            }
        }

        // Window resize event listener - grafikleri yeniden çiz
        let resizeTimeout;
        window.addEventListener('resize', function() {
            clearTimeout(resizeTimeout);
            resizeTimeout = setTimeout(function() {
                if (window.categoryScoresGlobal && window.categoryScoresGlobal.length > 0) {
                    const reportContainer = document.getElementById('reportContainer');
                    if (reportContainer.style.display === 'block') {
                        drawCharts();
                    }
                }
            }, 250);
        });

        // Sayfa yüklendiğinde login ekranını göster
        showLogin();
    </script>
</body>
</html>
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.8);
        z-index: 10000;
        overflow-y: auto;
        padding: 20px;
    ">
        <div style="
            max-width: 800px;
            margin: 30px auto;
            background: white;
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            position: relative;
        ">
            <button onclick="closeDisclaimerModal()" style="
                position: absolute;
                top: 15px;
                right: 15px;
                background: #f5576c;
                color: white;
                border: none;
                width: 35px;
                height: 35px;
                border-radius: 50%;
                font-size: 20px;
                cursor: pointer;
                line-height: 1;
            ">×</button>
            
            <h2 style="
                text-align: center;
                color: #667eea;
                margin-bottom: 20px;
                font-size: 1.8rem;
            ">⚖️ Sorumluluk Reddi, Gizlilik ve Veri Güvenliği Beyanı</h2>
            
            <div style="
                max-height: 500px;
                overflow-y: auto;
                padding: 20px;
                background: #f9f9f9;
                border-radius: 10px;
                margin-bottom: 25px;
                line-height: 1.8;
                font-size: 0.95rem;
            ">
                <p style="margin-bottom: 15px;">
                    Bu belge, <strong>Akça Pro X</strong> ve/veya <strong>Analiz Pro X</strong> platformları ile <strong>Barış Akça</strong> tarafından sunulan <strong>Kariyer Gelişim Çerçevesi (KGC)</strong> test/analiz sonuçlarının kullanımına ilişkin yasal sorumluluk sınırlarını ve veri güvenliği ilkelerini belirlemektedir.
                </p>
                
                <h3 style="color: #667eea; margin-top: 25px; margin-bottom: 15px; font-size: 1.3rem;">1. Veri Güvenliği ve Gizlilik Taahhüdü</h3>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">1.1. Veri Saklama ve Altyapı:</h4>
                <p style="margin-bottom: 15px;">
                    Tüm test ve analiz sonuçları, güvenilir ve yüksek standartlı bir bulut veri tabanı olan <strong>Google Firebase Firestore</strong> üzerinde saklanmaktadır. Veriler, Firebase'in güvenlik protokolleri ile korunmaktadır.
                </p>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">1.2. Kimlik Doğrulama ve Güvenlik:</h4>
                <p style="margin-bottom: 15px;">
                    Sisteme giriş, yalnızca güvenilir ve merkezi bir kimlik doğrulama yöntemi olan <strong>Google Girişi (Google Sign-In)</strong> kullanılarak sağlanır. Bu yöntem, kullanıcı güvenliğini en üst düzeyde tutmayı amaçlar.
                </p>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">1.3. Kişisel Veri Kullanımı ve Rumuz:</h4>
                <p style="margin-bottom: 15px;">
                    Platform, kullanıcıların <strong>Ad ve Soyadı</strong> gibi doğrudan kimlik bilgilerini talep etmez ve kullanmaz. Sisteme kayıt ve sonuçların ilişkilendirilmesi, kullanıcının belirlediği bir <strong>Rumuz</strong> veya otomatik olarak atanan bir <strong>kullanıcı kimliği (User ID)</strong> aracılığıyla gerçekleştirilir. Bu, anonimliği ve mahremiyeti destekler.
                </p>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">1.4. Veri Erişim Kısıtlaması:</h4>
                <p style="margin-bottom: 10px;">Test ve analiz sonuçlarına erişim kesinlikle kısıtlanmıştır:</p>
                <ul style="margin-left: 20px; margin-bottom: 15px;">
                    <li style="margin-bottom: 8px;"><strong>Kullanıcı:</strong> Kendi sonuçlarını görüntüleyebilir ve değerlendirebilir.</li>
                    <li style="margin-bottom: 8px;"><strong>Sistem Yöneticisi:</strong> Yalnızca sistemin işleyişini, teknik bütünlüğünü sağlamak ve kullanıcıya talep etmesi durumunda profesyonel danışmanlık hizmeti sunmak amacıyla sonuçlara erişim yetkisine sahiptir.</li>
                </ul>
                
                <h3 style="color: #667eea; margin-top: 25px; margin-bottom: 15px; font-size: 1.3rem;">2. Analiz Sonuçlarının Kullanımına İlişkin Sorumluluk Reddi</h3>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">2.1. Testin Amacı ve Niteliği:</h4>
                <p style="margin-bottom: 15px;">
                    Bu <strong>Kariyer Gelişim Çerçevesi (KGC)</strong>, gençlerin öz-farkındalık, potansiyel keşfi ve düşünce yapısını tetikleme amacıyla tasarlanmış profesyonel bir araçtır. <strong>Test sonuçları, bir profesyonel kariyer planının veya tıbbi/psikolojik bir tanının yerini tutmaz.</strong>
                </p>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">2.2. Kullanıcı Sorumluluğu ve Aksiyon Planı:</h4>
                <p style="margin-bottom: 15px;">
                    Kullanıcı, test sonuçlarına dayanarak <strong>tek başına herhangi bir kesin kariyer kararı veya aksiyon planı belirlememelidir</strong>. Test sonuçlarının hatalı veya eksik yorumlanması, kullanıcı için uygun olmayan kararlara ve dolayısıyla hatalı sonuçlara yol açabilir.
                </p>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">2.3. Profesyonel Danışmanlık İhtiyacı:</h4>
                <p style="margin-bottom: 15px;">
                    Kullanıcının, KGC sonuçlarını kariyer yolculuğuna entegre etmesi ve bu sonuçlara dayanarak anlamlı, sağlam adımlar atması için <strong>mutlaka lisanslı ve/veya yetkili bir profesyonel danışmanlık hizmeti alması şiddetle tavsiye edilir.</strong>
                </p>
                
                <h4 style="color: #764ba2; margin-top: 20px; margin-bottom: 10px;">2.4. Sorumluluk Sınırlaması:</h4>
                <p style="margin-bottom: 15px; padding: 15px; background: #fff3cd; border-left: 4px solid #ffc107; border-radius: 8px;">
                    <strong>⚠️ ÖNEMLİ:</strong> Kullanıcının, <strong>Akça Pro X</strong>, <strong>Analiz Pro X</strong> ve <strong>Barış Akça</strong>'dan bağımsız olarak, sadece kendi yorumlarına dayanarak attığı adımlar, aldığı kararlar veya uyguladığı planlar sonucunda ortaya çıkacak her türlü maddi, manevi veya kariyerle ilgili olumsuz sonuçtan doğan sorumluluk <strong>tamamen kullanıcıya aittir</strong>.
                </p>
                
                <p style="margin-bottom: 15px; padding: 15px; background: #fee; border-left: 4px solid #f5576c; border-radius: 8px;">
                    <strong>Akça Pro X</strong>, <strong>Analiz Pro X</strong> ve <strong>Barış Akça</strong>, ancak ve ancak profesyonel danışmanlık hizmetinin resmi olarak alındığı ve belgelendirildiği durumlar haricinde, test sonuçlarının yorumlanması ve uygulanmasından kaynaklanan <strong>hiçbir zarardan sorumlu tutulamaz</strong>.
                </p>
            </div>
            
            <div id="disclaimerActions" style="text-align: center; margin-top: 20px;">
                <label style="
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    gap: 10px;
                    margin-bottom: 20px;
                    font-size: 1rem;
                    cursor: pointer;
                ">
                    <input type="checkbox" id="disclaimerAccept" style="
                        width: 20px;
                        height: 20px;
                        cursor: pointer;
                    ">
                    <span>Okudum, anladım ve kabul ediyorum</span>
                </label>
                
                <button onclick="acceptDisclaimer()" id="acceptDisclaimerBtn" disabled style="
                    background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
                    color: white;
                    border: none;
                    padding: 12px 40px;
                    font-size: 1.1rem;
                    border-radius: 50px;
                    cursor: not-allowed;
                    opacity: 0.5;
                    transition: all 0.3s ease;
                ">
                    ✅ Onaylıyorum ve Devam Et
                </button>
            </div>
        </div>
    </div>
    
</body>
</html>
