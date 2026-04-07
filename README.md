html_content = '''<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🎬 Complete Content Creation Masterclass - Part 2</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Arial', 'Helvetica', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            line-height: 1.8;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            padding: 50px;
            box-shadow: 0 25px 70px rgba(0,0,0,0.4);
        }
        
        .header {
            text-align: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 50px;
            border-radius: 20px;
            margin-bottom: 50px;
            color: white;
        }
        
        .header h1 {
            font-size: 3.5em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .header .subtitle {
            font-size: 1.5em;
            opacity: 0.95;
            margin-bottom: 30px;
        }
        
        .part-badge {
            display: inline-block;
            background: #feca57;
            color: #333;
            padding: 10px 25px;
            border-radius: 25px;
            font-weight: bold;
            font-size: 1.2em;
            margin-bottom: 20px;
        }
        
        .toc {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 50px;
            border-left: 5px solid #667eea;
        }
        
        .toc h2 {
            color: #667eea;
            margin-bottom: 20px;
            font-size: 2em;
        }
        
        .toc ol {
            padding-left: 25px;
        }
        
        .toc li {
            margin: 12px 0;
            font-size: 1.15em;
            line-height: 1.6;
        }
        
        .toc li strong {
            color: #667eea;
        }
        
        .module {
            margin-bottom: 60px;
            padding: 40px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 20px;
            border-left: 8px solid #667eea;
        }
        
        .module-header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 3px solid #667eea;
        }
        
        .module-number {
            background: #667eea;
            color: white;
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2em;
            font-weight: bold;
            flex-shrink: 0;
        }
        
        .module-title {
            flex: 1;
        }
        
        .module-title h2 {
            color: #667eea;
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        
        .module-title p {
            color: #6c757d;
            font-size: 1.2em;
        }
        
        .section {
            margin: 35px 0;
        }
        
        .section h3 {
            color: #495057;
            font-size: 1.8em;
            margin-bottom: 20px;
            padding-left: 20px;
            border-left: 4px solid #feca57;
        }
        
        .section h4 {
            color: #667eea;
            font-size: 1.4em;
            margin: 25px 0 15px 0;
        }
        
        .content-block {
            background: white;
            padding: 25px;
            border-radius: 12px;
            margin: 20px 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .content-block p {
            margin-bottom: 15px;
            font-size: 1.1em;
            line-height: 1.8;
        }
        
        .content-block ul, .content-block ol {
            margin: 15px 0;
            padding-left: 30px;
        }
        
        .content-block li {
            margin: 10px 0;
            font-size: 1.05em;
            line-height: 1.7;
        }
        
        .highlight-box {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            padding: 25px;
            border-radius: 12px;
            margin: 25px 0;
            border-left: 5px solid #ff6b6b;
        }
        
        .highlight-box.success {
            background: linear-gradient(135deg, #d4fc79 0%, #96e6a1 100%);
            border-left-color: #4caf50;
        }
        
        .highlight-box.warning {
            background: linear-gradient(135deg, #ffeaa7 0%, #fdcb6e 100%);
            border-left-color: #f39c12;
        }
        
        .highlight-box.info {
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            border-left-color: #667eea;
        }
        
        .highlight-box h4 {
            margin-top: 0;
            margin-bottom: 15px;
            font-size: 1.3em;
        }
        
        .example-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }
        
        .example-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            border-top: 4px solid #667eea;
        }
        
        .example-card h5 {
            color: #667eea;
            font-size: 1.2em;
            margin-bottom: 15px;
        }
        
        .example-card .label {
            display: inline-block;
            background: #667eea;
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9em;
            margin-bottom: 12px;
        }
        
        .step-process {
            counter-reset: step-counter;
            margin: 30px 0;
        }
        
        .step {
            background: white;
            padding: 25px;
            border-radius: 12px;
            margin: 20px 0;
            position: relative;
            padding-left: 80px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .step::before {
            counter-increment: step-counter;
            content: counter(step-counter);
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
            background: #667eea;
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
            font-weight: bold;
        }
        
        .step h4 {
            margin-top: 0;
            color: #667eea;
            font-size: 1.3em;
            margin-bottom: 12px;
        }
        
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            margin: 25px 0;
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .comparison-table th {
            background: #667eea;
            color: white;
            padding: 15px;
            text-align: left;
            font-size: 1.1em;
        }
        
        .comparison-table td {
            padding: 15px;
            border-bottom: 1px solid #e9ecef;
        }
        
        .comparison-table tr:last-child td {
            border-bottom: none;
        }
        
        .comparison-table tr:nth-child(even) {
            background: #f8f9fa;
        }
        
        .key-takeaway {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
            margin: 30px 0;
            text-align: center;
        }
        
        .key-takeaway h4 {
            color: white;
            font-size: 1.6em;
            margin-bottom: 15px;
        }
        
        .key-takeaway p {
            font-size: 1.2em;
            line-height: 1.7;
        }
        
        .action-checklist {
            background: white;
            padding: 25px;
            border-radius: 12px;
            margin: 25px 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .action-checklist h4 {
            color: #667eea;
            margin-bottom: 20px;
            font-size: 1.4em;
        }
        
        .action-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            padding: 15px;
            margin: 10px 0;
            background: #f8f9fa;
            border-radius: 8px;
            border-left: 4px solid #4caf50;
        }
        
        .action-item input[type="checkbox"] {
            margin-top: 5px;
            width: 20px;
            height: 20px;
            cursor: pointer;
        }
        
        .action-item label {
            flex: 1;
            font-size: 1.05em;
            cursor: pointer;
        }
        
        .pro-tip {
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 100%);
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
            border-left: 5px solid #ff6b6b;
        }
        
        .pro-tip strong {
            color: #d63031;
            font-size: 1.1em;
        }
        
        .workflow-diagram {
            background: white;
            padding: 30px;
            border-radius: 12px;
            margin: 25px 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .workflow-step {
            display: flex;
            align-items: center;
            gap: 20px;
            margin: 20px 0;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }
        
        .workflow-icon {
            background: #667eea;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
            flex-shrink: 0;
        }
        
        .workflow-content {
            flex: 1;
        }
        
        .workflow-content h5 {
            color: #667eea;
            margin-bottom: 8px;
            font-size: 1.2em;
        }
        
        .tool-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 25px 0;
        }
        
        .tool-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            border-top: 4px solid #667eea;
        }
        
        .tool-card h5 {
            color: #667eea;
            font-size: 1.3em;
            margin-bottom: 15px;
        }
        
        .tool-card .category {
            display: inline-block;
            background: #667eea;
            color: white;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.85em;
            margin-bottom: 12px;
        }
        
        .platform-comparison {
            background: white;
            padding: 25px;
            border-radius: 12px;
            margin: 25px 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .platform-row {
            display: grid;
            grid-template-columns: 150px 1fr;
            gap: 20px;
            padding: 20px;
            margin: 15px 0;
            background: #f8f9fa;
            border-radius: 10px;
            align-items: center;
        }
        
        .platform-name {
            font-weight: bold;
            color: #667eea;
            font-size: 1.2em;
        }
        
        .metric-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.08);
        }
        
        .metric-card .number {
            font-size: 2em;
            font-weight: bold;
            color: #667eea;
            margin-bottom: 8px;
        }
        
        .metric-card .label {
            color: #6c757d;
            font-size: 0.95em;
        }
        
        .final-cta {
            text-align: center;
            padding: 50px;
            background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
            border-radius: 20px;
            color: white;
            margin-top: 50px;
        }
        
        .final-cta h2 {
            font-size: 2.8em;
            margin-bottom: 20px;
        }
        
        .final-cta p {
            font-size: 1.3em;
            line-height: 1.8;
            margin: 15px 0;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 25px;
            }
            
            .header h1 {
                font-size: 2.2em;
            }
            
            .module {
                padding: 25px;
            }
            
            .module-title h2 {
                font-size: 1.8em;
            }
            
            .example-grid,
            .tool-grid {
                grid-template-columns: 1fr;
            }
            
            .platform-row {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="part-badge">PART 2 of 2</div>
            <h1>🎬 Complete Content Creation Masterclass</h1>
            <p class="subtitle">Advanced Strategies: AI Workflows, Batching, Distribution & Analytics</p>
            <p style="font-size: 1.1em; margin-top: 20px; opacity: 0.9;">Modules 5-8: Scale Your Content & Maximize Your Reach</p>
        </div>
        
        <div class="toc">
            <h2>📚 Part 2 Modules</h2>
            <ol start="5">
                <li><strong>Module 5:</strong> AI-Enhanced Content Creation Workflow</li>
                <li><strong>Module 6:</strong> Content Batching & Production Systems</li>
                <li><strong>Module 7:</strong> Multi-Platform Distribution Strategy</li>
                <li><strong>Module 8:</strong> Analytics, Optimization & Continuous Improvement</li>
            </ol>
        </div>
        
        <!-- MODULE 5 -->
        <div class="module">
            <div class="module-header">
                <div class="module-number">5</div>
                <div class="module-title">
                    <h2>AI-Enhanced Content Creation</h2>
                    <p>Leverage AI tools to create more content in less time</p>
                </div>
            </div>
            
            <div class="section">
                <h3>The AI Content Revolution</h3>
                
                <div class="content-block">
                    <p>AI isn't replacing creators—it's <strong>amplifying</strong> them. The creators who embrace AI tools are producing 10x more content while maintaining quality. Here's how to join them.</p>
                    
                    <div class="highlight-box info">
                        <h4>🤖 The AI Advantage</h4>
                        <p><strong>Traditional Creator:</strong> 1-2 videos per day, 8 hours of work</p>
                        <p><strong>AI-Enhanced Creator:</strong> 5-10 videos per day, 4 hours of work</p>
                        <p style="margin-top: 15px; font-weight: bold;">Same quality. Half the time. 5x the output.</p>
                    </div>
                </div>
                
                <div class="content-block">
                    <h4>AI Tools Every Creator Needs</h4>
                    <p>These tools form the foundation of an AI-enhanced workflow:</p>
                </div>
                
                <div class="tool-grid">
                    <div class="tool-card">
                        <span class="category">Ideation</span>
                        <h5>ChatGPT / Claude</h5>
                        <p><strong>Use for:</strong></p>
                        <ul>
                            <li>Hook generation</li>
                            <li>Script writing</li>
                            <li>Content ideas</li>
                            <li>Trend analysis</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time saved:</strong> 2-3 hours/day</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Visuals</span>
                        <h5>Midjourney / DALL-E</h5>
                        <p><strong>Use for:</strong></p>
                        <ul>
                            <li>Thumbnails</li>
                            <li>Background images</li>
                            <li>Visual concepts</li>
                            <li>Brand assets</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time saved:</strong> 1-2 hours/day</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Video</span>
                        <h5>Runway / Pika</h5>
                        <p><strong>Use for:</strong></p>
                        <ul>
                            <li>B-roll generation</li>
                            <li>Transitions</li>
                            <li>Visual effects</li>
                            <li>Motion graphics</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time saved:</strong> 2-4 hours/day</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Editing</span>
                        <h5>CapCut / Descript</h5>
                        <p><strong>Use for:</strong></p>
                        <ul>
                            <li>Auto-captions</li>
                            <li>Quick cuts</li>
                            <li>Audio cleanup</li>
                            <li>Template editing</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time saved:</strong> 3-5 hours/day</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Voice</span>
                        <h5>ElevenLabs / Murf</h5>
                        <p><strong>Use for:</strong></p>
                        <ul>
                            <li>Voiceovers</li>
                            <li>Narration</li>
                            <li>Multi-language</li>
                            <li>Voice cloning</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time saved:</strong> 1-2 hours/day</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Analytics</span>
                        <h5>TubeBuddy / VidIQ</h5>
                        <p><strong>Use for:</strong></p>
                        <ul>
                            <li>Performance tracking</li>
                            <li>Keyword research</li>
                            <li>Competitor analysis</li>
                            <li>Optimization tips</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time saved:</strong> 1 hour/day</p>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3>The AI Loop System</h3>
                
                <div class="content-block">
                    <h4>What Are AI Loops?</h4>
                    <p>AI loops are rotating visual sequences that keep your content dynamic and engaging. Instead of static visuals, you cycle through AI-generated scenes that maintain viewer attention.</p>
                </div>
                
                <div class="workflow-diagram">
                    <h4 style="color: #667eea; margin-bottom: 20px;">Basic Loop Structure</h4>
                    
                    <div class="workflow-step">
                        <div class="workflow-icon">1</div>
                        <div class="workflow-content">
                            <h5>Creator Presence</h5>
                            <p>You appear on screen delivering your message (5-10 seconds)</p>
                        </div>
                    </div>
                    
                    <div class="workflow-step">
                        <div class="workflow-icon">2</div>
                        <div class="workflow-content">
                            <h5>AI Visual Transition</h5>
                            <p>Smooth transition to AI-generated cinematic scene (3-5 seconds)</p>
                        </div>
                    </div>
                    
                    <div class="workflow-step">
                        <div class="workflow-icon">3</div>
                        <div class="workflow-content">
                            <h5>Animated Storytelling</h5>
                            <p>AI-generated graphics or animations support your point (5-8 seconds)</p>
                        </div>
                    </div>
                    
                    <div class="workflow-step">
                        <div class="workflow-icon">4</div>
                        <div class="workflow-content">
                            <h5>Return to Creator</h5>
                            <p>Back to you for the next point or conclusion (5-10 seconds)</p>
                        </div>
                    </div>
                    
                    <div class="workflow-step">
                        <div class="workflow-icon">🔁</div>
                        <div class="workflow-content">
                            <h5>Loop Repeats</h5>
                            <p>Cycle continues throughout the video maintaining engagement</p>
                        </div>
                    </div>
                </div>
                
                <div class="highlight-box success">
                    <h4>✅ Why AI Loops Work</h4>
                    <ul>
                        <li><strong>Retention boost:</strong> Moving visuals keep viewers watching 2-3x longer</li>
                        <li><strong>Professional look:</strong> Elevates production value without expensive equipment</li>
                        <li><strong>Atmosphere creation:</strong> Sets mood and tone for your content</li>
                        <li><strong>Viewer rewards:</strong> Create custom loops for supporters and top fans</li>
                    </ul>
                </div>
                
                <div class="pro-tip">
                    <strong>💡 Pro Tip:</strong> Create a library of 20-30 AI loop templates. Mix and match them across videos to maintain consistency while keeping content fresh. Viewers will recognize your style without getting bored.
                </div>
            </div>
            
            <div class="section">
                <h3>AI Workflow Integration</h3>
                
                <div class="content-block">
                    <h4>The Complete AI-Enhanced Production Process</h4>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Ideation (AI-Powered)</h4>
                        <p><strong>Tools:</strong> ChatGPT, Claude, Perplexity</p>
                        <p><strong>Process:</strong></p>
                        <ul>
                            <li>Input your niche and target audience</li>
                            <li>Generate 50 content ideas in 5 minutes</li>
                            <li>Refine top 10 ideas with detailed outlines</li>
                            <li>Create hooks for each idea</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 15 minutes (vs 2 hours manually)</p>
                    </div>
                    
                    <div class="step">
                        <h4>Scripting (AI-Assisted)</h4>
                        <p><strong>Tools:</strong> ChatGPT, Claude</p>
                        <p><strong>Process:</strong></p>
                        <ul>
                            <li>Feed AI your content outline</li>
                            <li>Generate full script with hook, value, CTA</li>
                            <li>Edit for your voice and style</li>
                            <li>Create multiple versions for testing</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 10 minutes per script (vs 30-45 minutes)</p>
                    </div>
                    
                    <div class="step">
                        <h4>Visual Creation (AI-Generated)</h4>
                        <p><strong>Tools:</strong> Midjourney, DALL-E, Runway</p>
                        <p><strong>Process:</strong></p>
                        <ul>
                            <li>Generate thumbnails (5 variations)</li>
                            <li>Create B-roll visuals</li>
                            <li>Design graphics and overlays</li>
                            <li>Generate loop animations</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 20 minutes (vs 2-3 hours)</p>
                    </div>
                    
                    <div class="step">
                        <h4>Recording (You + AI)</h4>
                        <p><strong>Tools:</strong> Your camera + AI backgrounds</p>
                        <p><strong>Process:</strong></p>
                        <ul>
                            <li>Record yourself delivering script</li>
                            <li>Use AI-generated backgrounds</li>
                            <li>Record multiple takes quickly</li>
                            <li>AI removes background noise</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 30 minutes for 5 videos</p>
                    </div>
                    
                    <div class="step">
                        <h4>Editing (AI-Accelerated)</h4>
                        <p><strong>Tools:</strong> CapCut, Descript, Runway</p>
                        <p><strong>Process:</strong></p>
                        <ul>
                            <li>Auto-generate captions</li>
                            <li>AI removes filler words</li>
                            <li>Auto-add B-roll at key moments</li>
                            <li>Apply template effects</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 15 minutes per video (vs 1-2 hours)</p>
                    </div>
                </div>
                
                <div class="highlight-box warning">
                    <h4>⚠️ The Human Touch Rule</h4>
                    <p>AI should <strong>enhance</strong> your content, not replace you. Your personality, voice, and unique perspective are what make you stand out. Use AI for:</p>
                    <ul style="margin-top: 10px;">
                        <li>✅ Speed and efficiency</li>
                        <li>✅ Visual enhancement</li>
                        <li>✅ Idea generation</li>
                        <li>✅ Technical tasks</li>
                    </ul>
                    <p style="margin-top: 15px;">But always inject YOUR personality, stories, and authentic voice. That's what builds connection.</p>
                </div>
            </div>
            
            <div class="action-checklist">
                <h4>✅ Action Items: Implement AI Workflow</h4>
                <div class="action-item">
                    <input type="checkbox" id="ai1">
                    <label for="ai1">Sign up for 3 AI tools (ChatGPT, Midjourney, CapCut)</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="ai2">
                    <label for="ai2">Generate 50 content ideas using AI in one session</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="ai3">
                    <label for="ai3">Create 20 AI loop templates for your content library</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="ai4">
                    <label for="ai4">Produce your first video using the complete AI workflow</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="ai5">
                    <label for="ai5">Track time saved vs traditional methods</label>
                </div>
            </div>
            
            <div class="key-takeaway">
                <h4>🔑 Key Takeaway</h4>
                <p>AI tools are force multipliers. They don't replace creativity—they amplify it. The creators who master AI workflows will dominate the next era of content creation. Start small, experiment often, and scale what works.</p>
            </div>
        </div>
        
        <!-- MODULE 6 -->
        <div class="module">
            <div class="module-header">
                <div class="module-number">6</div>
                <div class="module-title">
                    <h2>Content Batching Systems</h2>
                    <p>Produce a week's worth of content in a single session</p>
                </div>
            </div>
            
            <div class="section">
                <h3>Why Batching Changes Everything</h3>
                
                <div class="content-block">
                    <p>Content batching is the secret weapon of successful creators. Instead of creating content daily (stressful, inconsistent), you create in focused batches (efficient, sustainable).</p>
                    
                    <div class="example-grid">
                        <div class="example-card" style="border-top-color: #ff6b6b;">
                            <h5>❌ Daily Creation (Burnout Path)</h5>
                            <p><strong>Monday:</strong> Brainstorm, film, edit, post (3 hours)</p>
                            <p><strong>Tuesday:</strong> Brainstorm, film, edit, post (3 hours)</p>
                            <p><strong>Wednesday:</strong> Brainstorm, film, edit, post (3 hours)</p>
                            <p><strong>Thursday:</strong> Too tired, skip</p>
                            <p><strong>Friday:</strong> Rushed content, low quality</p>
                            <p style="margin-top: 15px; font-weight: bold; color: #d63031;">Result: Burnout in 2 weeks</p>
                        </div>
                        
                        <div class="example-card" style="border-top-color: #4caf50;">
                            <h5>✅ Batch Creation (Sustainable Path)</h5>
                            <p><strong>Monday:</strong> Batch session - 10 videos (4 hours)</p>
                            <p><strong>Tuesday:</strong> Edit all 10 videos (3 hours)</p>
                            <p><strong>Wed-Sun:</strong> Auto-post, engage, live streams</p>
                            <p><strong>Next Monday:</strong> Repeat batch session</p>
                            <p style="margin-top: 15px; font-weight: bold; color: #27ae60;">Result: Sustainable for years</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3>The Perfect Batch Session</h3>
                
                <div class="content-block">
                    <h4>Pre-Batch Preparation (30 minutes)</h4>
                    <p>Success starts before you hit record:</p>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Choose Your Topic Cluster</h4>
                        <p>Pick ONE broad topic that can be broken into 5-10 subtopics.</p>
                        <p><strong>Example:</strong> "TikTok Growth" breaks into:</p>
                        <ul>
                            <li>Hook formulas</li>
                            <li>Posting times</li>
                            <li>Engagement strategies</li>
                            <li>Algorithm secrets</li>
                            <li>Common mistakes</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Write All Your Hooks</h4>
                        <p>Before filming, write hooks for all videos in the batch.</p>
                        <p><strong>Why:</strong> Maintains momentum, ensures variety, prevents creative blocks mid-session</p>
                    </div>
                    
                    <div class="step">
                        <h4>Set Up Your Space</h4>
                        <p>Optimize your filming environment once:</p>
                        <ul>
                            <li>Lighting positioned</li>
                            <li>Camera angle locked</li>
                            <li>Background arranged</li>
                            <li>Props ready</li>
                            <li>Outfit on</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Critical:</strong> Don't change ANYTHING during the batch</p>
                    </div>
                </div>
                
                <div class="content-block">
                    <h4>The Batch Recording Session (2-3 hours)</h4>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Warm Up (5 minutes)</h4>
                        <p>Record 2-3 practice takes to get comfortable on camera. Delete these—they're just warm-ups.</p>
                    </div>
                    
                    <div class="step">
                        <h4>Record in Sequence (90-120 minutes)</h4>
                        <p><strong>The system:</strong></p>
                        <ul>
                            <li>Record video 1 (3 takes maximum)</li>
                            <li>Immediately record video 2 (3 takes maximum)</li>
                            <li>Continue through all videos</li>
                            <li>No editing, no reviewing—just record</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Target:</strong> 5-10 videos in one session</p>
                    </div>
                    
                    <div class="step">
                        <h4>Quick Review (15 minutes)</h4>
                        <p>Watch each video once to ensure:</p>
                        <ul>
                            <li>Audio is clear</li>
                            <li>You're in frame</li>
                            <li>No major mistakes</li>
                        </ul>
                        <p style="margin-top: 12px;">If something is unusable, re-record immediately while setup is still ready.</p>
                    </div>
                </div>
                
                <div class="pro-tip">
                    <strong>💡 Pro Tip:</strong> Energy management is key. Your first 3 videos will be your best. Schedule your most important content first. By video 8-10, you'll be tired—save simpler content for the end.
                </div>
            </div>
            
            <div class="section">
                <h3>Batch Editing Workflow</h3>
                
                <div class="content-block">
                    <h4>The Assembly Line Approach</h4>
                    <p>Edit all videos in stages, not one at a time:</p>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Stage 1: Import & Organize (15 minutes)</h4>
                        <ul>
                            <li>Import all footage</li>
                            <li>Label each video clearly</li>
                            <li>Create project folders</li>
                            <li>Backup raw footage</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Stage 2: Rough Cuts (45 minutes)</h4>
                        <ul>
                            <li>Cut all videos to length</li>
                            <li>Remove dead space</li>
                            <li>Select best takes</li>
                            <li>No effects yet—just cuts</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Stage 3: Add Captions (30 minutes)</h4>
                        <ul>
                            <li>Use AI auto-caption tool</li>
                            <li>Apply to all videos</li>
                            <li>Quick proofread</li>
                            <li>Same style across all</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Stage 4: Effects & B-Roll (45 minutes)</h4>
                        <ul>
                            <li>Add transitions</li>
                            <li>Insert B-roll</li>
                            <li>Apply color grading</li>
                            <li>Add music/sound effects</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Stage 5: Export & Schedule (30 minutes)</h4>
                        <ul>
                            <li>Export all videos</li>
                            <li>Create thumbnails</li>
                            <li>Write captions</li>
                            <li>Schedule posts</li>
                        </ul>
                    </div>
                </div>
                
                <div class="highlight-box success">
                    <h4>✅ Batch Editing Benefits</h4>
                    <ul>
                        <li><strong>Faster:</strong> 3 hours for 10 videos vs 5 hours doing them individually</li>
                        <li><strong>Consistent:</strong> All videos have the same style and quality</li>
                        <li><strong>Efficient:</strong> You're in "editing mode" the whole time</li>
                        <li><strong>Less context switching:</strong> No mental fatigue from changing tasks</li>
                    </ul>
                </div>
            </div>
            
            <div class="section">
                <h3>Batching Best Practices</h3>
                
                <div class="content-block">
                    <h4>The Rules That Make Batching Work</h4>
                </div>
                
                <div class="example-grid">
                    <div class="example-card">
                        <h5>🎯 Rule 1: Same Setup</h5>
                        <p>Never change your setup mid-batch:</p>
                        <ul>
                            <li>Same outfit</li>
                            <li>Same lighting</li>
                            <li>Same background</li>
                            <li>Same camera angle</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Why:</strong> Consistency = professional look</p>
                    </div>
                    
                    <div class="example-card">
                        <h5>⏰ Rule 2: Time Blocks</h5>
                        <p>Protect your batch time:</p>
                        <ul>
                            <li>No phone calls</li>
                            <li>No social media</li>
                            <li>No interruptions</li>
                            <li>Deep focus only</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Why:</strong> Momentum is everything</p>
                    </div>
                    
                    <div class="example-card">
                        <h5>📊 Rule 3: Realistic Goals</h5>
                        <p>Start small, scale up:</p>
                        <ul>
                            <li>Week 1: 3 videos</li>
                            <li>Week 2: 5 videos</li>
                            <li>Week 3: 7 videos</li>
                            <li>Week 4: 10 videos</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Why:</strong> Build stamina gradually</p>
                    </div>
                    
                    <div class="example-card">
                        <h5>🔄 Rule 4: Weekly Rhythm</h5>
                        <p>Create a predictable schedule:</p>
                        <ul>
                            <li>Monday: Batch filming</li>
                            <li>Tuesday: Batch editing</li>
                            <li>Wed-Sun: Engage & post</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Why:</strong> Routine = sustainability</p>
                    </div>
                </div>
            </div>
            
            <div class="action-checklist">
                <h4>✅ Action Items: Master Content Batching</h4>
                <div class="action-item">
                    <input type="checkbox" id="batch1">
                    <label for="batch1">Choose your first topic cluster (1 broad topic → 10 subtopics)</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="batch2">
                    <label for="batch2">Write hooks for all 10 videos before filming</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="batch3">
                    <label for="batch3">Schedule a 3-hour batch filming session</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="batch4">
                    <label for="batch4">Complete your first batch edit using the 5-stage process</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="batch5">
                    <label for="batch5">Schedule all videos for the week ahead</label>
                </div>
            </div>
            
            <div class="key-takeaway">
                <h4>🔑 Key Takeaway</h4>
                <p>Batching isn't just about efficiency—it's about sustainability. The creators who last years (not months) are the ones who build systems that prevent burnout. Batch your content, protect your energy, and play the long game.</p>
            </div>
        </div>
        
        <!-- MODULE 7 -->
        <div class="module">
            <div class="module-header">
                <div class="module-number">7</div>
                <div class="module-title">
                    <h2>Multi-Platform Distribution</h2>
                    <p>Turn one video into 20+ pieces of content across all platforms</p>
                </div>
            </div>
            
            <div class="section">
                <h3>The Platform Multiplication Strategy</h3>
                
                <div class="content-block">
                    <p>Most creators make one video and post it to one platform. Smart creators make one video and distribute it to 5+ platforms. Elite creators turn that one video into 20+ pieces of content.</p>
                    
                    <div class="highlight-box info">
                        <h4>🚀 The Multiplication Effect</h4>
                        <p><strong>Average Creator:</strong> 1 video = 1,000 views on TikTok</p>
                        <p><strong>Multi-Platform Creator:</strong> Same video = 5,000 views across 5 platforms</p>
                        <p><strong>Elite Creator:</strong> 1 video → 20 pieces = 50,000+ total views</p>
                        <p style="margin-top: 15px; font-weight: bold;">Same effort. 50x the reach.</p>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3>Platform-Specific Optimization</h3>
                
                <div class="content-block">
                    <h4>Each Platform Has Different Rules</h4>
                    <p>Don't just copy-paste. Optimize for each platform's algorithm and audience:</p>
                </div>
                
                <div class="platform-comparison">
                    <div class="platform-row">
                        <div class="platform-name">TikTok</div>
                        <div>
                            <p><strong>Optimal Length:</strong> 15-60 seconds</p>
                            <p><strong>Best Times:</strong> 7-9am, 12-2pm, 7-11pm</p>
                            <p><strong>Key Metric:</strong> Watch time & completion rate</p>
                            <p><strong>Caption Strategy:</strong> Hook in first line, 3-5 hashtags max</p>
                        </div>
                    </div>
                    
                    <div class="platform-row">
                        <div class="platform-name">Instagram Reels</div>
                        <div>
                            <p><strong>Optimal Length:</strong> 7-30 seconds (shorter = better)</p>
                            <p><strong>Best Times:</strong> 11am-1pm, 7-9pm</p>
                            <p><strong>Key Metric:</strong> Saves & shares</p>
                            <p><strong>Caption Strategy:</strong> Longer captions work, 5-10 hashtags</p>
                        </div>
                    </div>
                    
                    <div class="platform-row">
                        <div class="platform-name">YouTube Shorts</div>
                        <div>
                            <p><strong>Optimal Length:</strong> 15-60 seconds</p>
                            <p><strong>Best Times:</strong> 2-4pm, 8-10pm</p>
                            <p><strong>Key Metric:</strong> Click-through to long-form</p>
                            <p><strong>Caption Strategy:</strong> SEO-focused title, keyword-rich description</p>
                        </div>
                    </div>
                    
                    <div class="platform-row">
                        <div class="platform-name">Facebook Reels</div>
                        <div>
                            <p><strong>Optimal Length:</strong> 30-60 seconds</p>
                            <p><strong>Best Times:</strong> 1-3pm, 7-9pm</p>
                            <p><strong>Key Metric:</strong> Shares & comments</p>
                            <p><strong>Caption Strategy:</strong> Question-based, encourage discussion</p>
                        </div>
                    </div>
                    
                    <div class="platform-row">
                        <div class="platform-name">LinkedIn</div>
                        <div>
                            <p><strong>Optimal Length:</strong> 30-90 seconds</p>
                            <p><strong>Best Times:</strong> 7-9am, 12-1pm, 5-6pm (weekdays)</p>
                            <p><strong>Key Metric:</strong> Professional engagement</p>
                            <p><strong>Caption Strategy:</strong> Professional tone, industry insights</p>
                        </div>
                    </div>
                </div>
                
                <div class="pro-tip">
                    <strong>💡 Pro Tip:</strong> Create platform-specific versions. Change the first 3 seconds for each platform to match what performs best there. The rest can stay the same.
                </div>
            </div>
            
            <div class="section">
                <h3>Content Multiplication Framework</h3>
                
                <div class="content-block">
                    <h4>Turn 1 Video Into 20+ Pieces</h4>
                    <p>Here's how to maximize every piece of content you create:</p>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Primary Distribution (5 platforms)</h4>
                        <p>Post the full video to all major platforms:</p>
                        <ul>
                            <li>TikTok</li>
                            <li>Instagram Reels</li>
                            <li>YouTube Shorts</li>
                            <li>Facebook Reels</li>
                            <li>LinkedIn (if B2B)</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Result:</strong> 5 pieces from 1 video</p>
                    </div>
                    
                    <div class="step">
                        <h4>Clip Extraction (5-8 clips)</h4>
                        <p>Extract the best moments as standalone clips:</p>
                        <ul>
                            <li>Best quote (15 seconds)</li>
                            <li>Key teaching moment (20 seconds)</li>
                            <li>Funny moment (10 seconds)</li>
                            <li>Controversial take (15 seconds)</li>
                            <li>Call to action (10 seconds)</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Result:</strong> 5-8 additional pieces</p>
                    </div>
                    
                    <div class="step">
                        <h4>Static Content (3-5 pieces)</h4>
                        <p>Convert video content to images:</p>
                        <ul>
                            <li>Quote graphics (Instagram/Facebook)</li>
                            <li>Carousel posts (Instagram)</li>
                            <li>Infographics (Pinterest/LinkedIn)</li>
                            <li>Thumbnail variations</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Result:</strong> 3-5 image posts</p>
                    </div>
                    
                    <div class="step">
                        <h4>Text Content (2-3 pieces)</h4>
                        <p>Repurpose as written content:</p>
                        <ul>
                            <li>Twitter/X thread</li>
                            <li>LinkedIn article</li>
                            <li>Blog post</li>
                            <li>Email newsletter</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Result:</strong> 2-3 text pieces</p>
                    </div>
                    
                    <div class="step">
                        <h4>Community Content (2-3 pieces)</h4>
                        <p>Engage your community:</p>
                        <ul>
                            <li>Behind-the-scenes of making the video</li>
                            <li>Bloopers/outtakes</li>
                            <li>Extended version for loyal fans</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Result:</strong> 2-3 bonus pieces</p>
                    </div>
                </div>
                
                <div class="highlight-box success">
                    <h4>✅ The Math</h4>
                    <p><strong>1 Original Video Becomes:</strong></p>
                    <ul style="margin-top: 10px;">
                        <li>5 platform posts</li>
                        <li>+ 5-8 clips</li>
                        <li>+ 3-5 static posts</li>
                        <li>+ 2-3 text pieces</li>
                        <li>+ 2-3 community pieces</li>
                    </ul>
                    <p style="margin-top: 15px; font-size: 1.3em; font-weight: bold;">= 17-24 pieces of content from 1 video!</p>
                </div>
            </div>
            
            <div class="section">
                <h3>Automation & Scheduling</h3>
                
                <div class="content-block">
                    <h4>Tools to Automate Distribution</h4>
                </div>
                
                <div class="tool-grid">
                    <div class="tool-card">
                        <span class="category">Multi-Platform</span>
                        <h5>Repurpose.io</h5>
                        <p>Automatically distributes content to multiple platforms</p>
                        <p style="margin-top: 12px;"><strong>Best for:</strong> TikTok → YouTube, Instagram, Facebook</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Scheduling</span>
                        <h5>Later / Buffer</h5>
                        <p>Schedule posts across all platforms</p>
                        <p style="margin-top: 12px;"><strong>Best for:</strong> Planning content calendar weeks ahead</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Analytics</span>
                        <h5>Metricool</h5>
                        <p>Track performance across all platforms</p>
                        <p style="margin-top: 12px;"><strong>Best for:</strong> Understanding what works where</p>
                    </div>
                    
                    <div class="tool-card">
                        <span class="category">Clipping</span>
                        <h5>OpusClip</h5>
                        <p>AI extracts best clips automatically</p>
                        <p style="margin-top: 12px;"><strong>Best for:</strong> Long videos → short clips</p>
                    </div>
                </div>
            </div>
            
            <div class="action-checklist">
                <h4>✅ Action Items: Master Multi-Platform Distribution</h4>
                <div class="action-item">
                    <input type="checkbox" id="dist1">
                    <label for="dist1">Set up accounts on all 5 major platforms</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="dist2">
                    <label for="dist2">Take 1 video and create 20 pieces using the framework</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="dist3">
                    <label for="dist3">Sign up for a scheduling tool (Later, Buffer, or Metricool)</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="dist4">
                    <label for="dist4">Schedule 1 week of content across all platforms</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="dist5">
                    <label for="dist5">Track which platforms perform best for your niche</label>
                </div>
            </div>
            
            <div class="key-takeaway">
                <h4>🔑 Key Takeaway</h4>
                <p>Distribution is just as important as creation. You can have the best content in the world, but if only 1,000 people see it, you're leaving 99% of your potential reach on the table. Master multi-platform distribution and watch your growth explode.</p>
            </div>
        </div>
        
        <!-- MODULE 8 -->
        <div class="module">
            <div class="module-header">
                <div class="module-number">8</div>
                <div class="module-title">
                    <h2>Analytics & Optimization</h2>
                    <p>Use data to double your results every month</p>
                </div>
            </div>
            
            <div class="section">
                <h3>The Metrics That Actually Matter</h3>
                
                <div class="content-block">
                    <p>Most creators track vanity metrics (followers, likes). Elite creators track <strong>performance metrics</strong> that actually predict success.</p>
                    
                    <div class="highlight-box warning">
                        <h4>⚠️ Stop Tracking These (Vanity Metrics)</h4>
                        <ul>
                            <li>❌ Total followers (doesn't predict revenue)</li>
                            <li>❌ Total likes (doesn't predict engagement)</li>
                            <li>❌ Total views (doesn't predict quality)</li>
                        </ul>
                        <p style="margin-top: 15px; font-weight: bold;">These numbers feel good but don't drive growth.</p>
                    </div>
                    
                    <div class="highlight-box success">
                        <h4>✅ Start Tracking These (Performance Metrics)</h4>
                        <ul>
                            <li>✅ Average watch time (shows content quality)</li>
                            <li>✅ Completion rate (shows hook effectiveness)</li>
                            <li>✅ Share rate (shows value delivery)</li>
                            <li>✅ Save rate (shows usefulness)</li>
                            <li>✅ Comment rate (shows engagement)</li>
                            <li>✅ Follower growth rate (shows momentum)</li>
                        </ul>
                        <p style="margin-top: 15px; font-weight: bold;">These predict future success.</p>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3>The Analytics Dashboard</h3>
                
                <div class="content-block">
                    <h4>Track These Numbers Weekly</h4>
                    <p>Create a simple spreadsheet to track your key metrics:</p>
                </div>
                
                <table class="comparison-table">
                    <thead>
                        <tr>
                            <th>Metric</th>
                            <th>Target</th>
                            <th>What It Tells You</th>
                            <th>How to Improve</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Watch Time</strong></td>
                            <td>50%+</td>
                            <td>Content quality & relevance</td>
                            <td>Stronger hooks, faster pacing</td>
                        </tr>
                        <tr>
                            <td><strong>Completion Rate</strong></td>
                            <td>40%+</td>
                            <td>Hook effectiveness</td>
                            <td>Test different hooks</td>
                        </tr>
                        <tr>
                            <td><strong>Share Rate</strong></td>
                            <td>5%+</td>
                            <td>Value & shareability</td>
                            <td>More actionable tips</td>
                        </tr>
                        <tr>
                            <td><strong>Save Rate</strong></td>
                            <td>3%+</td>
                            <td>Usefulness</td>
                            <td>Educational content</td>
                        </tr>
                        <tr>
                            <td><strong>Comment Rate</strong></td>
                            <td>2%+</td>
                            <td>Engagement & discussion</td>
                            <td>Ask questions, be controversial</td>
                        </tr>
                        <tr>
                            <td><strong>Follower Growth</strong></td>
                            <td>5-10%/week</td>
                            <td>Overall momentum</td>
                            <td>Consistency + quality</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            
            <div class="section">
                <h3>The Optimization Loop</h3>
                
                <div class="content-block">
                    <h4>How to Improve Every Week</h4>
                    <p>Elite creators follow this weekly optimization process:</p>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Monday: Review Last Week's Data</h4>
                        <p>Analyze your top 3 and bottom 3 performing videos:</p>
                        <ul>
                            <li>What hooks did top videos use?</li>
                            <li>What topics performed best?</li>
                            <li>What length worked best?</li>
                            <li>What time of day got most views?</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 30 minutes</p>
                    </div>
                    
                    <div class="step">
                        <h4>Tuesday: Identify Patterns</h4>
                        <p>Look for trends across multiple weeks:</p>
                        <ul>
                            <li>Which hook formulas consistently work?</li>
                            <li>Which topics always perform?</li>
                            <li>Which posting times are best?</li>
                            <li>Which video lengths get best completion?</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 20 minutes</p>
                    </div>
                    
                    <div class="step">
                        <h4>Wednesday: Create Hypothesis</h4>
                        <p>Based on data, form a testable hypothesis:</p>
                        <ul>
                            <li>"If I use 'Nobody tells you' hooks, I'll get 2x views"</li>
                            <li>"If I post at 7pm instead of 2pm, I'll get better engagement"</li>
                            <li>"If I make videos 30 seconds instead of 60, completion will increase"</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> 15 minutes</p>
                    </div>
                    
                    <div class="step">
                        <h4>Thursday-Sunday: Test Hypothesis</h4>
                        <p>Create content specifically to test your hypothesis:</p>
                        <ul>
                            <li>Make 3-5 videos with the new approach</li>
                            <li>Keep everything else the same</li>
                            <li>Track results carefully</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Time:</strong> Normal content creation time</p>
                    </div>
                    
                    <div class="step">
                        <h4>Next Monday: Analyze Results</h4>
                        <p>Did your hypothesis work?</p>
                        <ul>
                            <li>If YES → Make it your new standard</li>
                            <li>If NO → Form a new hypothesis</li>
                            <li>If UNCLEAR → Test again with more videos</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Result:</strong> Continuous improvement every week</p>
                    </div>
                </div>
                
                <div class="pro-tip">
                    <strong>💡 Pro Tip:</strong> Only test ONE variable at a time. If you change the hook AND the length AND the posting time, you won't know what caused the improvement (or decline).
                </div>
            </div>
            
            <div class="section">
                <h3>Advanced Analytics Strategies</h3>
                
                <div class="content-block">
                    <h4>Competitor Analysis</h4>
                    <p>Learn from creators who are already winning:</p>
                </div>
                
                <div class="step-process">
                    <div class="step">
                        <h4>Find Your Top 5 Competitors</h4>
                        <p>Identify creators in your niche who are:</p>
                        <ul>
                            <li>Similar size or slightly bigger</li>
                            <li>Posting similar content</li>
                            <li>Getting consistent engagement</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Analyze Their Top Content</h4>
                        <p>For each competitor, study their top 10 videos:</p>
                        <ul>
                            <li>What hooks do they use?</li>
                            <li>What topics perform best?</li>
                            <li>What's their video structure?</li>
                            <li>What's their posting frequency?</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Identify Gaps</h4>
                        <p>Find opportunities they're missing:</p>
                        <ul>
                            <li>Topics they haven't covered</li>
                            <li>Angles they haven't tried</li>
                            <li>Formats they don't use</li>
                        </ul>
                    </div>
                    
                    <div class="step">
                        <h4>Adapt & Improve</h4>
                        <p>Don't copy—improve:</p>
                        <ul>
                            <li>Take their successful formula</li>
                            <li>Add your unique perspective</li>
                            <li>Make it better/deeper/funnier</li>
                            <li>Test on your audience</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <div class="section">
                <h3>The 80/20 Rule for Content</h3>
                
                <div class="content-block">
                    <p>After analyzing your data, you'll discover that 20% of your content drives 80% of your results. Here's how to leverage that:</p>
                </div>
                
                <div class="example-grid">
                    <div class="example-card">
                        <h5>📊 Identify Your 20%</h5>
                        <p>Look at your top 20% of videos:</p>
                        <ul>
                            <li>What do they have in common?</li>
                            <li>What topics?</li>
                            <li>What hooks?</li>
                            <li>What format?</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Action:</strong> Document the pattern</p>
                    </div>
                    
                    <div class="example-card">
                        <h5>🔄 Double Down</h5>
                        <p>Create more of what works:</p>
                        <ul>
                            <li>60% of content = proven winners</li>
                            <li>30% of content = variations</li>
                            <li>10% of content = experiments</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Action:</strong> Shift your content mix</p>
                    </div>
                    
                    <div class="example-card">
                        <h5>🗑️ Cut the Losers</h5>
                        <p>Stop creating what doesn't work:</p>
                        <ul>
                            <li>Topics that consistently flop</li>
                            <li>Formats that don't engage</li>
                            <li>Posting times that underperform</li>
                        </ul>
                        <p style="margin-top: 12px;"><strong>Action:</strong> Eliminate waste</p>
                    </div>
                </div>
                
                <div class="highlight-box success">
                    <h4>✅ The Result</h4>
                    <p>By focusing on your top 20% of content types and eliminating the bottom 80%, you'll:</p>
                    <ul style="margin-top: 10px;">
                        <li>Create less content</li>
                        <li>Get better results</li>
                        <li>Save time and energy</li>
                        <li>Grow faster</li>
                    </ul>
                </div>
            </div>
            
            <div class="action-checklist">
                <h4>✅ Action Items: Master Analytics & Optimization</h4>
                <div class="action-item">
                    <input type="checkbox" id="analytics1">
                    <label for="analytics1">Create a spreadsheet to track your 6 key metrics weekly</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="analytics2">
                    <label for="analytics2">Analyze your top 10 and bottom 10 videos—find patterns</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="analytics3">
                    <label for="analytics3">Identify your top 5 competitors and analyze their content</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="analytics4">
                    <label for="analytics4">Form one hypothesis and test it this week</label>
                </div>
                <div class="action-item">
                    <input type="checkbox" id="analytics5">
                    <label for="analytics5">Implement the 80/20 rule—focus on what works</label>
                </div>
            </div>
            
            <div class="key-takeaway">
                <h4>🔑 Key Takeaway</h4>
                <p>Data doesn't lie. Your feelings about what "should" work don't matter—only what actually works matters. The creators who win are the ones who let data guide their decisions, test constantly, and optimize relentlessly. Become obsessed with your metrics, and watch your growth accelerate.</p>
            </div>
        </div>
        
        <!-- FINAL CTA -->
        <div class="final-cta">
            <h2>🎉 You've Completed the Masterclass!</h2>
            <p>You now have everything you need to create viral content, build your brand, and grow your audience across all platforms.</p>
            
            <div style="margin: 40px 0;">
                <h3 style="font-size: 2em; margin-bottom: 20px;">📚 What You've Mastered:</h3>
                <div style="text-align: left; max-width: 600px; margin: 0 auto;">
                    <p><strong>✅ Module 1:</strong> Platform psychology & algorithm fundamentals</p>
                    <p><strong>✅ Module 2:</strong> 7 proven hook formulas that stop the scroll</p>
                    <p><strong>✅ Module 3:</strong> Perfect video structure & storytelling</p>
                    <p><strong>✅ Module 4:</strong> Visual brand identity & consistency</p>
                    <p><strong>✅ Module 5:</strong> AI-enhanced content creation workflow</p>
                    <p><strong>✅ Module 6:</strong> Content batching systems for sustainability</p>
                    <p><strong>✅ Module 7:</strong> Multi-platform distribution strategy</p>
                    <p><strong>✅ Module 8:</strong> Analytics & continuous optimization</p>
                </div>
            </div>
            
            <h3 style="font-size: 2em; margin: 30px 0 20px 0;">🚀 Your Next Steps:</h3>
            <div style="text-align: left; max-width: 600px; margin: 0 auto; font-size: 1.1em;">
                <p><strong>Week 1:</strong> Implement your visual brand identity & take reference photos</p>
                <p><strong>Week 2:</strong> Complete your first batch session (5-10 videos)</p>
                <p><strong>Week 3:</strong> Set up multi-platform distribution</p>
                <p><strong>Week 4:</strong> Start tracking analytics & optimizing</p>
            </div>
            
            <div style="margin-top: 50px; padding: 30px; background: rgba(255,255,255,0.2); border-radius: 15px;">
                <h3 style="font-size: 1.8em; margin-bottom: 15px;">💡 Remember:</h3>
                <p style="font-size: 1.2em; line-height: 1.8;">
                    Knowledge without action is worthless. You now have the blueprint—but success comes from implementation. Start with ONE module. Master it. Then move to the next.
                </p>
                <p style="font-size: 1.3em; font-weight: bold; margin-top: 20px;">
                    Consistency beats perfection. Start today. 🎬
                </p>
            </div>
        </div>
    </div>
</body>
</html>'''

