# PMS項目 - PSC/PMO會議 問題及答案準備（廣東話版）

**會議日期**: 明天
**出席者**: COO、CFO、MD、DMD（營運）、財務團隊、行政採購團隊、PSC及PMO成員
**簡報文件**: Project Docu/PMS - PSC meeting_Sep 30_V5.pptx

---

## 一、高層管理（COO/MD/DMD）可能提出的問題

### Q1: 點解我哋要換PMS系統？現有系統有咩問題？
**答案（廣東話）**:
- 現時用緊嘅Dataswift系統已經好舊，冇乜support同埋好多process都係手動做
- 主要痛點包括：
  - 太多人手操作，要用大量Excel同紙張文件，好容易出錯
  - 系統之間冇整合（PMS、Property Cube、e-Procurement），資料唔一致
  - 冇自動化審批流程，要用實體簽名同人手傳送文件
  - 睇唔到即時嘅業主、租客、物業資料
  - 冇辦法產生有用嘅management reports同analytics

### Q2: 新系統可以帶嚟咩實際效益？ROI係幾多？
**答案（廣東話）**:
**財務效益（以每年5億港幣revenue計算）**:
- DSO由30日減到25日 = 改善現金流約680萬港幣
- 壞賬由0.8%減到0.5% = 節省150萬港幣
- 遲交費收取率提升25% = 額外收入80萬港幣
- AR人手減40%（10人減到6人）= 節省200萬港幣
- 法律費用減少40% = 節省20萬港幣
- **每年總效益約1,100萬港幣**

**投資成本（第一年）**:
- 系統設置：80萬港幣
- 整合開發：50萬港幣
- 範本製作：10萬港幣
- 變革管理：20萬港幣
- 年度license：30萬港幣
- **第一年總投資：190萬港幣**

**ROI**: 回本期2.1個月，3年NPV 2,900萬港幣，IRR >400%

### Q3: Implementation需要幾耐？會唔會影響日常運作？
**答案（廣東話）**:
**時間表**:
- 2025年10月：設計及批准（4星期）✅ 已完成
- 2025年11月：揀vendor（3星期）
- 2025年12月-2026年1月：開發第一階段（6星期）- dunning engine、payment整合
- 2026年2月-3月：開發第二階段（6星期）- 通訊平台、workflow、dashboard
- 2026年4月：UAT及培訓（4星期）
- 2026年5月：試行（2星期）- 2個物業，約500個單位
- 2026年6月：全面推出（4星期）- 所有portfolio，10,000+單位
- **預計go-live：2026年6月1日（由批准起計7個月）**

**風險緩解**:
- 分階段推出，先pilot後full rollout
- 設有fallback plan，確保日常運作唔受影響
- 提供90日hypercare support
- 培訓團隊確保smooth transition

---

## 二、財務總監(CFO)可能提出的問題

### Q4: 新系統如何改善我哋嘅cash flow同collections？
**答案（廣東話）**:
**Late Payment Reminder自動化流程**:
- **自動催收ladder**：
  - D+3: 禮貌提醒（Email + SMS）- 無罰款
  - D+7: 第一次逾期通知
  - D+14: 第二次逾期通知 + 信件 - **開始收遲交費**（5%）
  - D+21: 電話跟進 - 警告可能暫停服務
  - D+30: 最後通知 - 啟動服務暫停
  - D+45: 律師信（需要經理批准）
  - D+60+: 轉介法律部/收數公司

**自動化功能**:
- 即時payment allocation（FPS整合，95%自動配對）
- 自動排除有爭議賬戶、分期付款計劃
- 實時監察payment status
- 自動產生case file畀legal referral

**預期改善**:
- 收款率（30日內）由88%提升到95%
- 人手處理由80%減到15%
- Dispute解決時間由12日減到5日

### Q5: 遲交費嘅計算同收取會唔會符合香港法例同DMC條款？
**答案（廣東話）**:
**完全符合香港市場慣例同法例**:
- 遲交費率：每月5%（符合大部分DMC條款的上限）
- 最低收費：50港幣（符合市場慣例）
- 所有收費都要符合租約/DMC條款
- 設有approval workflow：
  - 少於500港幣：系統自動批准
  - 多於500港幣：需要AR Manager批准
  - 減免/豁免：需要AR Manager批准
  - 撇賬(多於10,000港幣)：需要CFO批准

**法律合規**:
- 法律團隊已審核流程
- 符合PDPO（個人資料私隱條例）
- 完整audit trail記錄所有費用
- 有爭議處理機制保障租客權益

### Q6: 點樣確保financial reporting同audit requirements達標？
**答案（廣東話）**:
**完整嘅Audit Trail**:
- 所有交易、批准、修改都有immutable log
- 記錄包括：user、timestamp、reason、approval
- 7年資料保留期（符合香港statutory requirement）
- Role-based access control，防止未授權修改

**Reporting功能**:
- 可自訂dashboard同report template
- Real-time KPI monitoring
- 支援Power BI / Tableau整合
- Ad-hoc查詢同batch processing
- Export to Excel功能
- Multi-year、multi-entity reporting

**Month-end/Year-end Closing**:
- 自動化depreciation計算
- 自動產生financial statements
- Management analysis報告
- Audit trail reports for external auditors

---

## 三、營運部門（Operations MD/DMD）可能提出的問題

### Q7: 新系統會唔會令Property Managers同AR team嘅工作量增加？
**答案（廣東話）**:
**實際上會大幅減少工作量**:

**AR Team**:
- 由處理100%嘅cases減到只處理15-20%嘅exceptions
- 自動payment allocation節省大量時間
- Dashboard清楚顯示priority queue
- 自動reminder發送，唔使人手打電話/寫信
- **預計人手需求減40%，可以重新調配資源做更高價值嘅工作**

**Property Managers**:
- 只需要處理disputes同approval requests
- 有clear SLA tracking（5個工作天解決dispute）
- System會自動提醒，唔會miss deadline
- 所有資料同documents都係centralized
- **實際工作量應該減少，而且更有系統**

**培訓支援**:
- AR Team: 2日培訓（queue management、payment plans）
- Property Managers: 1日培訓（dispute handling、approvals）
- 提供user manual同helpdesk支援

### Q8: 如果租客投訴話收到太多催收信點算？
**答案（廣東話）**:
**系統有完善嘅控制機制**:

**頻率控制**:
- 每星期最多1次提醒
- 唔會係週末或公眾假期發送
- 只會係香港營業時間打電話(09:00-18:00)

**自動排除機制**:
- 有active dispute：自動暫停催收
- 已有payment plan：只發installment提醒
- VIP/政府/特別安排賬戶：可以manual hold
- 已付款：即時停止催收（real-time payment update）

**PDPO合規**:
- 所有通訊都有consent記錄
- 提供unsubscribe選項（但payment notice係legal requirement）
- 只用於payment-related通訊
- 有complaint處理機制

**語氣分級**:
- 初期係禮貌提醒，唔係demanding
- 逐步escalate，確保fair warning
- 所有template都經過legal review
- 中英文雙語，確保租客明白

### Q9: 點樣處理有爭議嘅賬單？
**答案（廣東話）**:
**完整嘅Dispute Resolution Workflow**:

**流程**:
1. 租客raise dispute → 系統自動暫停催收
2. 分配畀Property Manager（有SLA timer）
3. PM調查：
   - 查租約/DMC
   - 查service delivery records
   - 查meter readings/utility bills
   - 查correspondence history
4. 決定：
   - **Valid dispute**: Issue credit note、調整billing、道歉
   - **Invalid dispute**: 提供詳細解釋、恢復催收

**SLA承諾**:
- 初步回應：2個工作天
- 完整調查：5個工作天
- 複雜cases：10個工作天（有interim updates）

**常見爭議類型**（香港market）:
- 管理費計算錯誤
- Service charge爭議（設施唔available）
- Meter reading錯誤（水電煤）
- 未授權收費
- 重複收費

**系統支援**:
- 一鍵flag dispute
- 自動通知PM同AR team
- Complete case notes同documents
- Audit trail記錄整個resolution過程

---

## 四、行政及採購團隊可能提出的問題

### Q10: Vendor selection process係點樣？點解揀呢個vendor？
**答案（廣東話）**:
**Vendor評估準則**:

**主要候選vendor**:
- MRI Software
- Kingdee（金蝶）

**評估準則**（按重要性排序）:
1. **Functional fit** (40%)：
   - 符合我哋嘅requirements checklist幾多%
   - Out-of-box功能 vs 需要customization
   - 支援香港specific requirements（FPS、bilingual、PDPO）

2. **Technical capability** (25%)：
   - Cloud infrastructure（AWS/Azure HK region）
   - Integration capabilities（APIs、data security）
   - Scalability同performance
   - Mobile support

3. **Implementation & Support** (20%)：
   - Implementation timeline同methodology
   - Local support team（香港office）
   - Training同documentation
   - Track record in HK property management market

4. **Commercial** (15%)：
   - Total Cost of Ownership（TCO）
   - Licensing model（per user vs per unit）
   - Professional services cost
   - Annual maintenance/support fees

**選擇流程**:
- RFP已發出，收到2個vendors嘅proposal
- Demo已完成（7月同8月）
- Deep-dive workshops已進行
- Requirements checklist comparison已完成
- **預計11月作最終決定**

### Q11: 新系統嘅licensing cost同ongoing費用係幾多？
**答案（廣東話）**:
**Cost breakdown（估算）**:

**一次性費用**:
- System configuration: 80萬港幣
- Integration development: 50萬港幣（FPS、email、SMS、payments）
- Template creation: 10萬港幣（bilingual、design、legal review）
- Change management: 20萬港幣（training、communications、helpdesk）
- **一次性總投資：160萬港幣**

**年度經常費用**:
- SaaS licensing: 
  - 按units計（~10,000 units）或
  - 按users計（~50-100 users）
  - 預計：20-25萬港幣/年
- Communications platform（email/SMS）: 3萬港幣/年
- Infrastructure（cloud hosting）: 2萬港幣/年
- Annual maintenance/support: 5萬港幣/年
- **年度總費用：約30萬港幣**

**對比現有系統**:
- 現有Dataswift維護費：~15萬港幣/年
- 增加：~15萬港幣/年
- 但效益係1,100萬港幣/年，非常抵！

### Q12: 如果vendor唔再support或執笨點算？
**答案（廣東話）**:
**風險緩解措施**:

**Vendor穩定性**:
- MRI同Kingdee都係established vendors
- MRI：全球最大嘅property management software公司
- Kingdee：上市公司（香港交易所），financial穩定
- 兩者都有香港local office同support team

**合約保障**:
- Source code escrow agreement（如果vendor執笨可以拎code）
- Data ownership明確（我哋own所有data）
- Data export功能（可以隨時export去第二個系統）
- Service Level Agreement（SLA）with penalties

**技術保障**:
- 用standard APIs同open architecture
- 避免proprietary lock-in
- Cloud hosting by AWS/Azure（唔係vendor own infrastructure）
- Regular data backup（daily incremental、weekly full）

**Business Continuity Plan**:
- 如果系統down，有manual fallback procedures
- Backup communication providers（email/SMS）
- 7年data retention in archive

---

## 五、IT/技術相關問題

### Q13: 新系統嘅security同data privacy如何保障？
**答案（廣東話）**:
**完全符合香港法例同國際標準**:

**PDPO (Personal Data Privacy Ordinance) 合規**:
- 所有tenant data收集都有consent（in lease agreement）
- Purpose limitation：只用於payment collection
- 唔會同第三方分享（除非legal/DCA with consent）
- Tenant有權查閱、更正自己嘅資料
- 7年retention period（statutory requirement）

**Technical Security**:
- **Encryption**: AES-256 at rest、TLS 1.3 in transit
- **Access Control**: Role-based access control (RBAC)
- **Authentication**: MFA (Multi-Factor Authentication)、SSO support
- **Audit**: Complete audit trail（immutable logs）
- **PII Masking**: Reports同dashboard會mask個人資料
- **Data Sovereignty**: 資料存放係Hong Kong region（AWS/Azure HK）

**Infrastructure Security**:
- Cloud provider（AWS/Azure）有ISO 27001、SOC 2 certification
- Regular security assessments同penetration testing
- DDoS protection、firewall、intrusion detection
- Disaster recovery plan（RPO < 1 hour、RTO < 4 hours）

**Compliance Audits**:
- Annual security audit
- PDPO compliance review by legal team
- Regular vulnerability scanning
- Incident response plan

### Q14: 新系統點樣整合現有systems？
**答案（廣東話）**:
**主要整合需求**:

**1. Payment Gateways**:
- **FPS (Faster Payment System)**: Real-time整合，用unique payment reference
- **Bank files**: Daily import（Autopay、telegraphic transfer）
- **Credit card processors**: Visa/Master/AMEX
- **E-wallets**: Alipay、WeChat Pay、Octopus

**2. Property Cube**:
- Master data sync（property、unit、owner、tenant info）
- Bidirectional sync確保資料一致
- API-based integration（REST APIs）

**3. e-Procurement System**:
- Vendor master data sync
- Purchase order同invoice matching
- Budget control integration

**4. HRIS (Human Resources)**:
- User authentication（SSO）
- Role同permission sync
- Employee master data

**5. Communication Platforms**:
- Email service（SendGrid / AWS SES）
- SMS gateway（香港telecom providers）
- Document management system

**Integration Architecture**:
- 用standard REST APIs同webhooks
- Real-time integration for payments（FPS）
- Batch integration for others（daily/hourly）
- Error handling同retry mechanism
- Integration monitoring dashboard

**Testing**:
- Integration testing in UAT environment
- End-to-end testing of all workflows
- Performance testing（10,000+ units）

---

## 六、項目管理辦公室(PMO)可能提出的問題

### Q15: Project governance structure係點樣？邊個負責make decisions？
**答案（廣東話）**:
**Governance Structure**:

**1. Project Steering Committee (PSC)**:
- **成員**: CFO（chair）、Head of Operations、IT Director、Legal Counsel
- **職責**: 
  - 批准major decisions（vendor selection、budget、timeline）
  - 解決escalated issues
  - Review project status（monthly）
  - Sign-off on major milestones
- **會議**: Monthly或as needed

**2. Project Management Office (PMO)**:
- **成員**: Project Manager、Business Analyst、IT Lead、Change Manager
- **職責**:
  - Day-to-day project management
  - Coordinate workstreams
  - Monitor progress、budget、risks
  - Report to PSC
- **會議**: Weekly project team meetings

**3. Subject Matter Experts (SMEs)**:
- AR Manager、Property Managers、Finance Manager
- 提供業務input同UAT
- 協助制定requirements同testing

**4. Vendor Project Team**:
- Vendor project manager、developers、consultants
- 負責system configuration、development、testing

**Decision-Making Framework**:
- **Strategic decisions**: PSC approval required（e.g., vendor selection、major scope changes）
- **Tactical decisions**: PMO can decide（e.g., minor config changes、test approach）
- **Technical decisions**: IT Lead + Vendor team（e.g., integration approach）
- **Business decisions**: SMEs + AR Manager（e.g., workflow details、templates）

### Q16: 點樣monitor project progress同risks？
**答案（廣東話）**:
**Project Monitoring**:

**1. Weekly Progress Tracking**:
- **Dashboard metrics**:
  - Milestones status (on track / at risk / delayed)
  - Budget vs actual spend
  - Resource utilization
  - Open issues/risks count
  - Deliverables completed %

**2. Risk Management**:
**Top Risks同Mitigation**:

| 風險 | 可能性 | 影響 | 緩解措施 |
|------|--------|------|----------|
| Vendor delay in development | Medium | High | Clear milestones with penalties; weekly progress review |
| Integration complexity | Medium | High | Early integration testing; expert consultants |
| User resistance to change | Medium | Medium | Extensive training; change champions; early involvement |
| Data migration issues | Low | High | Multiple test migrations; data quality checks |
| System downtime during cutover | Low | High | Pilot approach; fallback plan; extended support |

**3. Issue Management**:
- Issue log with priority、owner、due date
- Escalation path: Team → PMO → PSC
- Weekly review in project team meetings
- Monthly summary to PSC

**4. Change Control**:
- Change request process for scope changes
- Impact assessment (time、cost、resources)
- PSC approval for major changes
- Change log tracking

**5. Reporting**:
- **Weekly**: Status report to PMO（detailed）
- **Monthly**: Executive summary to PSC（high-level）
- **Ad-hoc**: Risk/issue escalation as needed

### Q17: User training同change management plan係點樣？
**答案（廣東話）**:
**Change Management Strategy**:

**1. Stakeholder Analysis**:
- **Champions**: AR Manager、senior Property Managers（early adopters）
- **Impacted users**: AR team、Property Managers、Finance team、IT support
- **Informed**: Senior management、tenants

**2. Communication Plan**:
**Internal**:
- **Pre-launch（-30 days）**: Project overview to all staff
- **-14 days**: Detailed workflow changes
- **-7 days**: Training schedule同access info
- **Launch day**: Go-live announcement
- **Post-launch**: Weekly tips、FAQ updates、success stories

**External（Tenants）**:
- **-30 days**: Letter通知新payment methods同portal
- **Launch**: Email/SMS announcement
- **Post-launch**: FAQ、helpdesk support、feedback collection

**3. Training Program**:

| 對象 | 時間 | 內容 | 形式 |
|------|------|------|------|
| AR Team | 2日 | Queue management、payment plans、escalation rules、reporting | Hands-on workshop |
| Property Managers | 1日 | Dispute handling、approval workflows、reporting | Workshop + demo |
| Finance Team | 0.5日 | KPIs、legal referrals、write-offs、financial reports | Presentation + Q&A |
| IT Support | 2日 | System admin、troubleshooting、integration monitoring | Technical training |
| Tenants | Self-service | Payment methods、online portal、FAQ | Video tutorials、user guide |

**4. Training Materials**:
- User manuals（中英文）
- Video tutorials（for common tasks）
- Quick reference guides（cheat sheets）
- FAQ documents
- Practice environment for hands-on learning

**5. Post-Launch Support**:
- **Hypercare period（90 days）**:
  - Dedicated helpdesk（hotline + email）
  - On-site support for first 2 weeks
  - Daily standup for issue resolution
  - Weekly feedback sessions
- **Knowledge base**: Build up FAQs同troubleshooting guides
- **Continuous improvement**: Collect feedback同optimize workflows

**6. Change Champions Network**:
- Identify champions in each department
- Early training同involvement
- Act as first line of support for peers
- Provide feedback for improvements

---

## 七、法律及合規問題

### Q18: 如果租客話唔想收SMS/email催收信點算？
**答案（廣東話）**:
**法律立場清晰**:

**Payment notice係legal obligation**:
- 根據rental agreement/DMC，landlord有權通知tenant outstanding payment
- PDPO有exemption for contractual obligations同debt collection
- Tenant唔可以完全opt-out payment notices

**但我哋會respect preferences**:
- **Capture preferences**: 
  - Preferred channel（email、SMS、letter、phone）
  - Preferred language（EN/ZH）
  - Preferred contact time
- **Marketing vs Payment**:
  - Payment notices: Cannot opt-out（legal requirement）
  - Marketing communications: Can opt-out（PDPO requirement）
- **Frequency control**:
  - 最多每星期1次
  - 唔會係不合理時間（深夜、週末）

**Complaint handling**:
- 如果tenant投訴harassment：
  - Review communication history
  - Check if frequency過多
  - 可以temporary hold催收（while investigate）
  - Adjust approach for specific tenant
- 有clear escalation path to Property Manager

**Documentation**:
- All consent同preferences stored in system
- Audit trail of all communications sent
- 可以show證據證明compliant

### Q19: Legal referral process係點確保齊晒required documents？
**答案（廣東話）**:
**自動產生完整case file**:

**系統會compile**:
1. **Full invoice history**: 
   - All outstanding invoices with dates、amounts
   - Payment history showing partial payments
   - Late fees applied同breakdown

2. **Communication history**:
   - All reminders sent（with dates、channels、content）
   - Delivery confirmations
   - Tenant responses（if any）

3. **Tenant information**:
   - Full contact details
   - HKID/passport number（for legal proceedings）
   - Employment/business info（if available）

4. **Property/Lease information**:
   - Lease agreement（original同renewals）
   - DMC terms relevant to payment同late fees
   - Property address同unit details
   - Landlord information

5. **Dispute history**:
   - Any disputes raised同how resolved
   - Credit notes issued
   - Special arrangements/payment plans

6. **Timeline summary**:
   - Chronological list of all key events
   - Easy for lawyer to understand case quickly

**Quality checks**:
- System validates all required fields before allow legal referral
- Manual checklist for PMO to verify completeness
- Legal team review before send to external lawyer/DCA

**Handoff process**:
- Secure portal for DCA/lawyer access
- PDF package with index
- Track legal case status in PMS
- Updates flow back to PMS

---

## 八、商業及策略問題

### Q20: 新系統會唔會畀我哋competitive advantage？
**答案（廣東話）**:
**絕對會！香港市場比較**:

| 指標 | Savills（現時） | 市場平均 | Savills（To-Be） | Best-in-Class |
|------|----------------|----------|-----------------|---------------|
| DSO | 30日 | 28日 | **25日** | 20-23日 |
| 自動配對rate | 40% | 60% | **95%** | 95%+ |
| 收款率（90日） | 92% | 94% | **97%** | 97-98% |
| AR效率 | 500 units/FTE | 700 units/FTE | **1,200 units/FTE** | 1,000-1,500/FTE |
| 壞賬率 | 0.8% | 0.6% | **0.5%** | 0.3-0.5% |

**成為industry leader**:
- 最自動化嘅collections process in HK property management
- 最好嘅tenant experience（transparent、bilingual、multi-channel）
- 最complete嘅compliance（PDPO、audit trail）
- 可以handle更多portfolio without增加headcount

**對生意發展嘅幫助**:
- **Pitch new clients**: 展示我哋嘅technology leadership
- **Operational efficiency**: 可以接更多projects without成本上升
- **Better decision making**: Real-time analytics同KPIs
- **Tenant satisfaction**: 好嘅experience增加renewal rate

### Q21: 如果經濟差，租客遲交payment增加，系統handle到嗎？
**答案（廣東話）**:
**系統專為呢啲situation而設計**:

**Scalability**:
- 可以handle 10,000+ overdue cases simultaneously
- Auto-prioritization by amount、age、tenant type
- AR team focus on high-value cases

**Flexible payment plans**:
- 系統可以offer installment plans
- Auto-monitor compliance
- 如果tenant miss一期，可以auto-escalate或adjust plan
- 對於經濟困難嘅tenant，提供flexibility可以improve eventual collection

**Portfolio management**:
- Dashboard顯示overall portfolio health
- Early warning indicators（collection rate dropping、DSO increasing）
- Predictive analytics（邊啲tenant可能會有問題）
- Proactive outreach to at-risk accounts

**香港市場經驗**:
- 我哋參考咗經濟週期嘅best practices
- 系統設計包括seasonality factors（Chinese New Year、Christmas collection rates低）
- 支援government relief schemes（如果再有rental relief）

**Resource reallocation**:
- 因為70%係automated，AR team有capacity處理volume上升
- 可以temporarily adjust dunning ladder（例如extend grace period）
- 系統夠flexible可以快速應對policy changes

---

## 九、實施細節問題

### Q22: Pilot phase會test啲咩？點知ready for full rollout？
**答案（廣東話）**:
**Pilot Parameters（5月2026，2個星期）**:

**Scope**:
- **Properties**: 2個properties（1 residential、1 commercial）
- **Units**: ~500 units
- **Users**: ~5-8 users（AR team、Property Managers）
- **Features**: 完整end-to-end workflow

**Success Criteria（Go/No-Go for Full Rollout）**:

| 指標 | Target | Measurement |
|------|--------|-------------|
| System uptime | >99% | Monitoring logs |
| Payment auto-allocation rate | >90% | Transaction logs |
| Reminder送達率 | >95% | Email/SMS delivery reports |
| User satisfaction | >80% positive | Survey |
| Critical bugs | 0 | Bug tracking system |
| Processing time | <5 mins for 100 accounts | Performance logs |

**Test Scenarios**:
1. **Normal flow**: Overdue invoices → reminders → payment → case closure
2. **Dispute handling**: Flag dispute → suspend dunning → PM resolve → resume
3. **Payment plan**: Partial payment → offer plan → monitor installments
4. **Escalation**: D+45 → final notice approval → legal referral
5. **Exception handling**: VIP account hold、manual adjustments
6. **Integration**: FPS payment → auto-allocation → receipt generation
7. **Reporting**: Generate all key reports同dashboards

**Risk mitigation during pilot**:
- Fallback to manual process if system fails
- Dedicated support team on standby
- Daily review meetings
- Quick fix for any issues
- 租客communication話係試行階段

**Go/No-Go Decision Point**:
- 2星期pilot結束時review
- PSC決定proceed或extend pilot
- 如果有major issues，fix後repeat pilot

### Q23: Data migration係咪好複雜？會唔會有data loss？
**答案（廣東話）**:
**Data Migration Strategy**:

**Phase 1: Data Inventory（Discovery）**:
- 清點現有Dataswift data：
  - Properties、units、owners、tenants
  - Leases、contracts、amendments
  - Invoices、receipts、payments
  - Vendors、purchase orders
  - Historical transactions（保留幾多年？）

**Phase 2: Data Quality Assessment**:
- Identify data issues：
  - Missing fields
  - Duplicates
  - Inconsistencies
  - Invalid formats
- **Data cleansing before migration**（可能需要1-2個月）

**Phase 3: Mapping & Transformation**:
- Map Dataswift fields to new system fields
- Define transformation rules（e.g., date formats、codes）
- Handle special cases

**Phase 4: Test Migrations（Multiple rounds）**:
1. **First test**: Small dataset（1 property）
2. **Second test**: Larger dataset（10 properties）
3. **Third test**: Full dataset（dry run）
- 每次test都驗證data integrity
- Identify同fix issues before real migration

**Phase 5: Cutover Migration**:
- 安排係weekend或public holiday
- Stop Dataswift transactions（freeze period）
- Run migration scripts
- Verify all data transferred correctly
- Parallel run for 1-2 months（both systems active）

**Data Loss Prevention**:
- **Complete backup** before migration
- **Verification checks** after migration：
  - Record counts match
  - Financial totals reconcile
  - Sample record spot checks
- **Reconciliation reports**
- **Rollback plan** if major issues found

**Parallel Run Period**:
- New system for new transactions
- Old system available for reference
- Daily reconciliation
- 1-2個月後fully cutover

---

## 十、總結同Next Steps

### Q24: 如果PSC approve，即刻要做咩？
**答案（廣東話）**:
**Immediate Actions（批准後首2星期）**:

**Week 1**:
1. ✅ **Finalize vendor selection**:
   - 最後evaluation（如果未決定）
   - 合約談判同簽署
   - PO發出

2. ✅ **Project kickoff**:
   - Kickoff meeting with vendor
   - Confirm project plan同milestones
   - Set up project governance（meetings、reporting）

3. ✅ **Team mobilization**:
   - Assign project team members
   - Set up project workspace（shared drive、Teams channel）
   - Schedule weekly project meetings

**Week 2**:
4. ✅ **Detailed requirements review**:
   - Walk through requirements with vendor
   - Identify any gaps或customizations needed
   - Prioritize features for each sprint

5. ✅ **Environment setup**:
   - Provision cloud infrastructure
   - Set up development、test、UAT environments
   - Configure access同security

6. ✅ **Data preparation**:
   - Start data inventory
   - Begin data cleansing
   - Prepare sample data for development

**Week 3-4**:
7. ✅ **Integration planning**:
   - Technical workshops on FPS、email、SMS integrations
   - Design integration architecture
   - Set up test accounts with payment gateways

8. ✅ **Template design**:
   - Draft dunning templates（EN/ZH）
   - Legal review
   - Design approval

9. ✅ **Change management launch**:
   - Communication to all staff about project
   - Identify change champions
   - Plan training schedule

**Critical Path Items（唔可以delay）**:
- Vendor contract簽署
- Cloud environment setup
- FPS integration approval（需要bank approval，可能要時間）
- Legal review of templates同T&Cs

### Q25: 我哋點樣measure success after go-live？
**答案（廣東話）**:
**Key Performance Indicators (KPIs)**:

**1. Financial KPIs**:
- **DSO**: Target <25 days（現時30 days）
- **Collection rate**:
  - 0-30 days: >95%（現時88%）
  - 31-60 days: >85%
  - 61-90 days: >70%
- **Bad debt write-off**: <0.5% of revenue（現時0.8%）
- **Late fee collection rate**: >85%（現時60%）

**2. Operational KPIs**:
- **Auto-allocation rate**: >95%（現時40%）
- **Manual intervention rate**: <15%（現時80%）
- **Right-party contact rate**: >90%
- **Email/SMS bounce rate**: <5%
- **Dispute resolution time**: <5 days（現時12 days）
- **Promise-to-pay kept ratio**: >80%

**3. Efficiency KPIs**:
- **AR staff productivity**: >1,000 units/FTE（現時500）
- **Same-day resolution**: >60% of disputes
- **Payment plan success rate**: >75%
- **Legal referral rate**: <2%

**4. User Experience KPIs**:
- **System uptime**: >99.5%
- **User satisfaction**: >80%（survey）
- **Tenant complaints**: <1% of accounts
- **Template personalization**: 100%（correct language）

**Measurement Frequency**:
- **Daily**: System uptime、critical transactions
- **Weekly**: Collection rates、case volumes、AR queue
- **Monthly**: Full KPI dashboard、trend analysis
- **Quarterly**: Business review with PSC

**Review Cadence**:
- **Week 1-4 post go-live**: Daily standups
- **Month 1-3 (Hypercare)**: Weekly reviews
- **Month 4-6**: Bi-weekly reviews
- **Month 7+**: Monthly reviews

**90-Day Post-Launch Review**:
- Compare actual vs target KPIs
- Identify areas for optimization
- Collect user feedback
- Fine-tune workflows、templates、thresholds
- Celebrate wins同learn from issues
- Plan continuous improvement roadmap

**Continuous Improvement**:
- A/B testing on templates（response rates）
- Optimize dunning ladder timing
- Enhance auto-allocation rules
- Add new payment methods as needed
- Expand analytics同predictive models

---

## 附加資源

### 重要文件參考
- 簡報文件：`Project Docu/PMS - PSC meeting_Sep 30_V5.pptx`
- Late Payment Design：`Late-Payment-Reminder-Design-Documentation.md`
- Executive Summary：`Late-Payment-Workflow-Executive-Summary.md`
- Swimlane Diagram：`Late-Payment-Reminder-Swimlane.drawio.xml`
- PWC Analysis：`PWC report/PWC - Savills User Requirements Review Over PMS v2.4 - clean.pdf`
- Vendor Comparison：`Vendor Proposal/PMS User Requirement Checklist – Comparison.xlsx`

### 關鍵數字速記
- **投資**: 第一年190萬港幣
- **回報**: 每年1,100萬港幣效益
- **ROI**: 2.1個月回本
- **時間**: 7個月到go-live（from approval）
- **DSO改善**: 30日 → 25日（5日改善）
- **自動化**: 80% manual → 15% manual（65%改善）

### 應對意外問題嘅Tips
如果有問題你唔sure答案：
1. **承認同跟進**: "呢個係好嘅問題，我會詳細check完之後盡快回覆你"
2. **Defer to experts**: "呢個技術細節我想請IT team詳細解釋"
3. **Reference documentation**: "詳細資料我哋有document，會後可以share畀大家"
4. **PSC決定**: "呢個涉及policy decision，我建議由PSC決定最合適"

### Presentation Tips
- 帶laptop backup（以防投影有問題）
- Print key pages做handout
- 預早15分鐘到setup
- 準備demo video（如果可以）
- 帶calculator（即場計數）
- 有questions list for Q&A session

**祝你presentation成功！💪**

