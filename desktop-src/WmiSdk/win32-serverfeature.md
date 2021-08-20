---
description: класс Win32 \_ ServerFeature представляет компоненты, установленные на компьютере, на котором работает Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Класс Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: eddbd71108a5b6b65de329e1c110c965f437e4c24f7ba0a681935ba5075351fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312141"
---
# <a name="win32_serverfeature-class"></a>\_Класс Win32 ServerFeature

\[Класс **Win32 \_ ServerFeature** доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [классы поставщика ServerManager deploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]

класс **Win32 \_ ServerFeature** представляет компоненты, установленные на компьютере, на котором работает Windows Server.

Этот класс может использоваться разработчиками и администраторами, которым необходимо автоматизировать процесс определения функций, установленных на наборе серверных компьютеров. Экземпляры этого класса недоступны на клиентских компьютерах.

## <a name="syntax"></a>Синтаксис

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ ServerFeature** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ ServerFeature** имеет следующие свойства.

<dl> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**ключ**](key-qualifier.md), а [**не \_ null**](optional-qualifiers.md)
</dt> </dl>

Идентификатор компонента сервера. В следующем списке приведены возможные значения свойства ID:



Значение

Имя

1

[Сервер приложений](/windows)

2

Веб-сервер (IIS)

3

[Службы потоков мультимедиа](/windows)

5

Факс-сервер

6

Файловые службы и службы iSCSI<br/> [изменение имени](/windows)<br/>

7

Службы печати и документов<br/> [изменение имени](/windows)<br/>

8

[Active Directory Federation Services](/windows) (Службы федерации Active Directory)

9

Службы Active Directory облегченного доступа к каталогам (AD LDS)

10

Доменные службы Active Directory

11

[Службы UDDI](/windows)<br/>

12

[DHCP-сервер](/windows)

13

[DNS-сервер](/windows)

14

Network Policy and Access Services

16

Службы сертификатов Active Directory

17

Службы управления правами Active Directory (AD RMS)

18

[Службы удаленных рабочих столов](/windows)<br/> [изменение имени](/windows)<br/>

19

Windows Deployment Services

20

Hyper-V

21

[Службы Windows Server Update Services](/windows)

33

[Отказоустойчивая кластеризация](/windows)

34

[Балансировка сетевой нагрузки](/windows)

36

[Компоненты .NET Framework 3.5.1](/windows)<br/> [изменение имени](/windows)<br/>

37

[Диспетчер системных ресурсов Windows](/windows)

38

Служба беспроводной локальной сети

39

[Windows Функции резервного копирования сервера](/windows)

40

WINS-сервер

41

Служба активации процессов Windows

42

[Удаленный помощник](/windows)

43

простые службы TCP/IP;

44

[Клиент Telnet](/windows)

45

[Сервер Telnet](/windows)

46

[Подсистема для приложений на базе UNIX](/windows)

47

Прокси-сервер RPC через HTTP

48

SMTP-сервер

49

служба очередей сообщений

51

[Внутренняя база данных Windows](/windows)

52

[служба хранилища Диспетчер для сетей SAN](/windows)

53

Монитор порта LPR

55

[Сервер имен интернет-хранилища](/windows)

57

[Multipath I/O](/windows)

58

TFTP-клиент

59

[Службы SNMP](/windows)

60

[диспетчер съемных служба хранилища](/windows)

61

Шифрование диска BitLocker

62

[Службы для сетевой файловой системы](/windows)

63

Клиент печати через Интернет

64

[Протокол PNRP](/windows)

65

Пакет администрирования диспетчера подключений

66

[Windows PowerShell](/windows)<br/>

67

[Средства удаленного администрирования сервера](/windows)

68

[qWave;](/windows)

69

[Управление групповой политикой](/windows)

71

[служба индексирования](/windows)

72

[Диспетчер ресурсов файлового сервера](/windows)

73

Протокол удаленного разностного сжатия

310

Службы рукописного ввода<br/>

320

[Средства миграции Windows Server](/windows)<br/>

321

[Расширение IIS WinRM](/windows)<br/>

324

[BranchCache,,](#branchcache)<br/>

334

[Консоль управления DirectAccess](/windows)<br/>

335

[Фоновая интеллектуальная служба передачи (BITS)](/windows)<br/>

338

[Средство просмотра XPS](/windows)<br/>

339

[Биометрическая платформа Windows](/windows)<br/>

340

Поддержка WoW64<br/>

351

[Windows PowerShell Интегрированная среда сценариев (ISE)](/windows)<br/>

352

Фильтры Windows TIFF IFilter<br/>

404

[Службы обновления Windows Server](/windows)

409

[Сервер управления IP-адресами (IPAM)](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Служба Windows Search](/windows)

438

[Клиент для NFS](/windows)

441

[Сетевая разблокировка BitLocker](/windows)

442

[Расширение IIS OData для управления](/windows)

450

[Дополнительные службы .NET Framework 4.5 Advanced Services](/windows)

466

[Компоненты .NET Framework 4.5](/windows)

468

[Удаленный доступ](/windows)<br/>

477

[Пользовательские интерфейсы и инфраструктура](/windows)

478

[графические средства управления и инфраструктура.](/windows)

481

[Файловые службы и службы хранилища](/windows)

485

[Режим Windows Server Essentials](/windows)

488

[Direct Play](/windows)

Файловые службы — службы ролей (6)

Значение

Имя

100

[распределенная файловая система](/windows)

101

Пространство имен DFS

102

Репликация DFS

103

[Служба репликации файлов](/windows)

104

[Диспетчер ресурсов файлового сервера](/windows)

105

[Службы для сетевой файловой системы](/windows)

106

[Хранилище единственных копий](/windows)

107

[Служба Windows Search](/windows)

108

[служба индексирования](/windows)

255

Файловый сервер

350

Служба BranchCache для сетевых файлов

431

[Сервер для NFS](/windows)<br/>

434

[Служба агента VSS файлового сервера](/windows)<br/>

435

[Целевой сервер iSCSI](/windows)<br/>

436

[Дедупликация данных](/windows)<br/>

437

[поставщик служба хранилища цели iSCSI (поставщики оборудования VDS и VSS)](/windows)

486

[Рабочие папки](/windows)

Службы ролей AD DS (10)

Значение

Имя

110

[Контроллер домена Active Directory](/windows)

111

[Управление удостоверениями для UNIX](/windows)

112

[Сервер для служб сведений о сети](/windows)

113

[Синхронизация паролей](/windows)

294

[Средства удаленного администрирования сервера](/windows)

Службы ролей потоковой передачи мультимедиа (3)

Значение

Имя

120

[Windows Сервер мультимедиа](/windows)

121

[Веб-администрирование](/windows)

122

[Агент ведения журнала](/windows)

ADFS — службы ролей (8)

Значение

Имя

125

[Active Directory Federation Services](/windows) (Службы федерации Active Directory)

126

[Политика служба федерации](/windows)

127

[Веб-агенты служб федерации Active Directory](/windows)

128

[Агент, поддерживающий утверждения](/windows)

129

[Агент, использующий токены Windows](/windows)

Службы ролей службы удаленных рабочих столов (18)

Значение

Имя

130

Узел сеансов удаленных рабочих столов<br/> [изменение имени](/windows)<br/>

131

[Лицензирование удаленных рабочих столов](/windows)<br/> [изменение имени](/windows)<br/>

132

Шлюз удаленных рабочих столов<br/> [изменение имени](/windows)<br/>

133

Посредник подключений к удаленному рабочему столу<br/> [изменение имени](/windows)<br/>

134

Веб-доступ к удаленным рабочим столам<br/> [изменение имени](/windows)<br/>

322

Узел виртуализации удаленных рабочих столов<br/>

Службы ролей Узел виртуализации удаленных рабочих столов (322)

Значение

Имя

325

[Основные службы](/windows)<br/>

327

[удаленный рабочий стол виртуальных графических элементов](/windows)<br/>

Службы ролей службы печати и документов (7)

Значение

Имя

135

Сервер печати

136

Печать через Интернет

137

Служба печати LPD

328

[Сервер распределенного сканирования](/windows)<br/>

Веб-сервер (IIS) — службы ролей (2)

Значение

Имя

140

Веб-сервер

141

Общие функции HTTP

142

Статическое содержимое

143

Документ по умолчанию

144

Обзор каталога

145

Ошибки HTTP

146

Перенаправление HTTP

147

Разработка приложений

148

ASP.NET

149

Расширяемость платформы .NET

150

ASP

151

CGI

152

Расширения ISAPI

153

Фильтры ISAPI

154

Включения на стороне сервера

155

Работоспособность и диагностика

156

Ведение журнала HTTP

157

Средства ведения журнала

158

Монитор запросов

159

Трассировка

160

Настраиваемое ведение журнала

161

Ведение журнала ODBC

162

Безопасность

163

Обычная проверка подлинности

164

Проверка подлинности Windows

165

Дайджест-проверка подлинности

166

Проверка подлинности с сопоставлением сертификата клиента

167

Аутентификация IIS с сопоставлением сертификата клиента

168

Авторизация URL-адресов

169

Фильтрация запросов

170

Ограничения IP-адресов и доменов

171

Производительность

172

Сжатие статического содержимого

173

Функция сжатия динамического содержимого

174

Средства управления

175

Консоль управления (IIS)

176

Сценарии и средства управления IIS

177

Служба Management Service

178

Совместимость управления IIS 6

179

Совместимость метабазы IIS 6

180

Совместимость с WMI IIS 6

181

Инструменты для работы со сценариев IIS 6

182

Консоль управления IIS 6

183

Служба FTP-публикаций<br/>

184

FTP-сервер

185

Консоль управления FTP<br/>

314

Публикация WebDAV

316

Служба FTP<br/>

317

Расширяемость FTP<br/>

336

Внедряемое веб-ядро служб IIS<br/>

413

[ASP.NET 4,5](/windows)

414

[Расширяемость .NET 4.5](/windows)

445

[аппиализатион](/windows)

446

[централизованная поддержка SSL-сертификатов](/windows)

447

[Протокол WebSocket](/windows)

Очередь сообщений — функции (49)

Значение

Имя

190

Службы очереди сообщений

191

Сервер службы очередей сообщений

192

Интеграция служб каталогов

193

Триггеры очереди сообщений

194

Поддержка HTTP

195

Служба маршрутизации

196

[поддержка клиентов Windows 2000](/windows)<br/>

197

DCOM-прокси очереди сообщений

228

Поддержка многоадресной рассылки

Службы сертификации Active Directory — службы ролей (16)

Значение

Имя

200

Центр сертификации

201

Служба регистрации в центре сертификации через Интернет

202

Сетевой ответчик

204

Служба подачи заявок на сетевые устройства

318

[Веб-служба регистрации сертификатов](/windows)<br/>

319

[веб-служба политик регистрации сертификатов](/windows)<br/>

политика сети и службы ролей службы Access (14)

Значение

Имя

205

[Сервер политики сети](/windows)

206

[VPN](#vpn)

207

[удаленный службы Access](/windows)

208

[Маршрутизация](#routing)

210

[Центр регистрации работоспособности](/windows)

250

[Протокол авторизации учетных данных узла](/windows)

Службы UDDI — службы ролей (11)

Значение

Имя

215

[Веб-приложение служб UDDI](/windows)<br/>

216

[База данных служб UDDI](/windows)<br/>

Windows Служба активации процессов — службы ролей (41)

Значение

Имя

217

API настройки

218

Среда .NET

219

Модель процесса

платформа .NET Framework 3.5.1 — функции (36)

Значение

Имя

220

.NET Framework 3.5.1<br/> [изменение имени](/windows)<br/>

221

Активация WCF

222

Активация по протоколам HTTP

223

Не-HTTP активация

227

Средство просмотра XPS<br/>

Службы SNMP — функции (59)

Значение

Имя

224

[служба SNMP;](/windows)

225

[Поставщик WMI SNMP](/windows)

Службы ролей Службы приложений

Значение

Имя

230

[.NET Framework 3.5.1](/windows)<br/> [изменение имени](/windows)<br/>

231

[Поддержка веб-сервера (IIS)](/windows)

232

[Доступ к сети COM+](/windows)

233

[Совместное использование TCP-портов](/windows)

234

[Windows Поддержка службы активации процессов](/windows)

235

[Активация по HTTP](/windows)

236

[Активация службы очередей сообщений](/windows)

237

[Активация TCP](/windows)

238

[Активация по именованным каналам](/windows)

239

[Распределенные транзакции](/windows)

240

[Входящие удаленные транзакции](/windows)

241

[Исходящие удаленные транзакции](/windows)

242

[WS-автоматические транзакции](/windows)

353

[Расширения сервера приложений для .NET 4,0](/windows)<br/>

Windows Службы развертывания — роль (19)

Значение

Имя

251

Сервер развертывания

252

Транспортный сервер

службы ролей службы Active Directory Rights Management (17)

Значение

Имя

253

Сервер управления правами Active Directory

254

Поддержка федерации удостоверений

Средства удаленного администрирования сервера (67)

Значение

Имя

256

[Средства администрирования ролей](/windows)

257

[Средства AD DS](/windows)<br/> [изменение имени](/windows)<br/>

258

[Средства Snap-Ins и Command-Line AD LDS](/windows)<br/> [изменение имени](/windows)<br/>

259

Средства служб сертификатов Active Directory

260

[Network Policy and Access Services](/windows)

261

Средства службы печати и документов<br/> [изменение имени](/windows)<br/>

262

[Службы управления правами Active Directory (AD RMS)](/windows)

263

[Средства служб удаленных рабочих столов](/windows)<br/> [изменение имени](/windows)<br/>

264

Windows Средства служб развертывания

265

[Средства администрирования компонентов](/windows)

266

Средства шифрования диска BitLocker

267

Средства серверных расширений BITS

268

[Средства отказоустойчивости кластеров](/windows)

269

Средства балансировки сетевой нагрузки

270

Средства SMTP-сервера

273

[Средства DNS-сервера](/windows)

277

Средства файловых служб

278

Средства распределенная файловая система

279

Средства диспетчер ресурсов файлового сервера

280

[Службы для средств сетевой файловой системы](/windows)

281

Средства веб-сервера (IIS)

284

[Средства хоста удаленный рабочий стол сеансов](/windows)<br/> [изменение имени](/windows)<br/>

285

Средства шлюза удаленный рабочий стол<br/> [изменение имени](/windows)<br/>

286

Средства лицензирования удаленный рабочий стол<br/> [изменение имени](/windows)<br/>

288

Средства факсового сервера

290

Средства WINS-сервера

291

[Средства служб UDDI](/windows)<br/>

292

Средства центра сертификации

293

Средства сетевого ответчика

297

[Средства сервера для NIS](/windows)

299

[Средства Snap-Ins и Command-Line AD DS](/windows)<br/> [изменение имени](/windows)<br/>

300

[Центр администрирования Active Directory](/windows)

301

Средства Hyper-V

323

[Средство просмотра паролей восстановления BitLocker](/windows)<br/>

326

[Средства администрирования шифрования диска BitLocker](/windows)<br/>

329

[Средства AD DS и AD LDS](/windows)<br/>

330

Центр администрирования Active Directory<br/>

331

[Модуль Active Directory для Windows PowerShell](/windows)<br/>

337

[Средства брокера подключение к удаленному рабочему столу](/windows)<br/>

410

[клиент управление IP-адресами (IPAM)](/windows)

450

[Модуль Hyper-V для Windows PowerShell](/windows)

462

[службы Active Directory Rights Management Инструментари](/windows)

465

[средство управления общими ресурсами и служба хранилища](/windows)

471

[Средства управления удаленным доступом](/windows)

472

[модуль удаленного доступа для Windows PowerShell.](/windows)

473

[Графический интерфейс удаленного доступа и средства Command-Line](/windows)

474

[Средства служб Windows Server Update Services](/windows)

476

[Средства диагностики лицензирования удаленный рабочий стол](/windows)

479

[Средства SNMP](/windows)

480

[Инструменты корпоративной активации](/windows)

Windows Резервное копирование сервера — функции (39)

Значение

Имя

296

[Система архивации данных Windows Server](/windows)

297

[Программы командной строки](/windows)

Функции службы рукописного ввода (310)

Значение

Имя

311

[Поддержка рукописного ввода](/windows)<br/>

312

[Распознавание рукописного текста](/windows)<br/>

Фоновая интеллектуальная служба передачи (BITS) — функции (335)

Значение

Имя

54

Расширение сервера IIS

332

[Облегченный сервер загрузки](/windows)<br/>

Поддержка WOW64 — функции (340)

Значение

Имя

341

[WoW64](#wow64)<br/>

342

[подсистема WoW64 для платформа .NET Framework 2,0 и Windows PowerShell](/windows)<br/>

343

[подсистема WoW64 для платформа .NET Framework 2,0](/windows)<br/>

344

[Подсистема WoW64 для PowerShell](/windows)<br/>

345

[подсистема WoW64 для платформа .NET Framework 3,0 и 3,5](/windows)<br/>

346

[Подсистема WoW64 для служб печати](/windows)<br/>

347

[Подсистема WoW64 для отказоустойчивой кластеризации](/windows)<br/>

348

[Подсистема WoW64 для редактора метода ввода](/windows)<br/>

349

[подсистема WoW64 для приложений на основе UNIX](/windows)<br/>

Пользовательские интерфейсы и инфраструктура — службы ролей (447)

Значение

Имя

35

[Возможности рабочего стола](/windows)

99

[Графическая оболочка сервера](/windows)

Службы Windows Server Update Services — функции (404)

Значение

Имя

405

[API и командлеты PowerShell](/windows)

406

[SQL Server Установлен](/windows)

407

[Службы WSUS](/windows)

408

[Консоль управления пользовательским интерфейсом](/windows)

449

[Подключение WID](/windows)

функции Windows PowerShell (417)

Значение

Имя

411

[подсистема Windows PowerShell 2,0](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Windows PowerShell Web Access](/windows)

1000

[служба Desired State Configuration Windows PowerShell](/windows)

платформа .NET Framework 4,5-функции (418)

Значение

Имя

419

[расширенная платформа .NET Framework 4,5](/windows)

420

[Службы WCF](/windows)

421

[Активация по HTTP](/windows)

422

[Активация очереди сообщений (MSMQ)](/windows)

423

[Активация именованного канала](/windows)

424

[Активация TCP](/windows)

425

[Совместное использование TCP-портов](/windows)

429

[ASP.NET 4,5](/windows)

Удаленный доступ — роль (468)

Значение

Имя

469

[DirectAccess и VPN (RAS)](/windows)

470

[Маршрутизация](#routing)

файловые и служба хранилищаные службы — роль (481)

Значение

Имя

482

[Службы хранилища](/windows)

484

[Средства управления отказоустойчивыми кластерами](/windows)



 

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Отображаемое имя компонента сервера, например "файловый сервер", "сервер печати" или "возможности рабочего стола".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

ИДЕНТИФИКАЦИОНный номер компонента родительского сервера. Это свойство равно 0, если функция, представленная текущим экземпляром класса, не имеет родительского компонента.

</dd> </dl>

## <a name="remarks"></a>Remarks

ознакомьтесь с [техническим обзором Windows server 2008 диспетчер сервера](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) , чтобы узнать о возможностях сервера.

предприятия, которые не используют программное обеспечение для управления, которое сообщает о возможностях сервера, например System Center Operations Manager с установленными пакетами управления, могут получить эту информацию, запросив класс **Win32 \_ ServerFeature** .

Функции удаленного взаимодействия WMI или WinRM можно использовать для получения сведений о компонентах сервера с удаленных серверов. Дополнительные сведения об удаленных DCOM-подключениях WMI см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md). Дополнительные сведения о WinRM см. в статье Windows Remote Management (Удаленное управление Windows).

Windows Server 2012: **Win32 \_ ServerFeature** является устаревшим. Для программного доступа к сведениям о компонентах Windows Server можно использовать [командлеты Диспетчер сервера](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).

### <a name="windows-server-2012-r2"></a>Windows Server 2012 R2

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Сервер приложений
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>потоковая передача Cлужбы мультимедиа
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>службы федерации Active Directory (AD FS)
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP-сервер
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS-сервер
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>службы удаленных рабочих столов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Отказоустойчивая кластеризация
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Балансировка сетевой нагрузки
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>функции платформа .NET Framework 3.5.1
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Системные диспетчер ресурсов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Функции резервного копирования сервера
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Удаленный помощник
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Клиент Telnet
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Сервер Telnet
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Подсистема для приложений на базе UNIX
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>внутренняя база данных Windows
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>служба хранилища Диспетчер для сетей SAN
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>сервер интернет служба хранилища имя
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Службы SNMP
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Службы для сетевой файловой системы
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Протокол разрешения имен одноранговых узлов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>средства удаленного администрирования сервера
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>качество звука Windows Audio Video
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Управление групповая политика
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Служба индексирования
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Диспетчер ресурсов файлового сервера (FSRM)
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Средства миграции сервера
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Консоль управления DirectAccess
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Фоновая интеллектуальная служба передачи (бит)
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Поддержка WoW64
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Службы обновления Windows Server
</dt> <dd>

Добавлено

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>сервер управление IP-адресами (IPAM)
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>платформа .NET Framework 4,5
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Служба поиска
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Клиент для NFS
</dt> <dd>

Добавлено

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Сетевая разблокировка BitLocker
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Расширение IIS OData для управления
</dt> <dd>

Добавлено

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>платформа .NET Framework 4,5 дополнительные службы
</dt> <dd>

Добавлено

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>функции платформа .NET Framework 4,5
</dt> <dd>

Добавлено

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Пользовательские интерфейсы и инфраструктура
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Графические средства управления и инфраструктура
</dt> <dd>

Добавлено

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>файловые и служба хранилищаные службы
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Интерфейс Essentials Server
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Прямое воспроизведение
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>распределенная файловая система
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>диспетчер ресурсов файлового сервера
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Службы для сетевой файловой системы
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>служба хранилища одного экземпляра
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Служба поиска
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Служба индексирования
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>поставщик служба хранилища цели iSCSI (поставщики оборудования VDS и VSS)
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Рабочие папки
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Контроллер домен Active Directory
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Управление удостоверениями для UNIX
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Сервер для служб сведений о сети
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Синхронизация паролей
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Средства администрирования
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Сервер мультимедиа
</dt> <dd>

Больше не поддерживается.

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Веб-администрирование
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Агент ведения журнала
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>служба федерации
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Политика служба федерации
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>Веб-агенты AD FS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Агент на основе токенов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Лицензирование удаленный рабочий стол
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Сервер политики сети
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>ЧЕРЕЗ
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>удаленный службы Access
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Маршруты
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Центр регистрации работоспособности
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Протокол авторизации учетных данных узла
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>платформа .NET Framework 3.5.1
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Средство просмотра XPS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Служба SNMP
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Поставщик WMI SNMP
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>платформа .NET Framework 3.5.1
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Поддержка веб-сервера (IIS)
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Доступ к сети COM+
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Совместное использование TCP-портов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Поддержка службы активации процессов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Активация по HTTP
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Активация службы очередей сообщений
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Активация по TCP
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Активация по именованным каналам
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Распределенные транзакции
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Входящие удаленные транзакции
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Исходящие удаленные транзакции
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-автоматические транзакции
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Расширения сервера приложений для .NET 4,0
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Средства администрирования ролей
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Средства AD DS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Средства Snap-Ins и Command-Line AD LDS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>сетевая политика и службы Access
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>службы Active Directory Rights Management
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Средства службы удаленных рабочих столов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Средства администрирования компонентов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Средства отказоустойчивой кластеризации
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Средства DNS-сервера
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Службы для средств сетевой файловой системы
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Средства веб-сервера (IIS)
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Средства сервера для NIS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Средства Snap-Ins и Command-Line AD DS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Средства AD DS и AD LDS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Средства брокера подключение к удаленному рабочему столу
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>клиент управление IP-адресами (IPAM)
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Модуль Hyper-V для Windows PowerShell
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>службы Active Directory Rights Management Утилит
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>средство управления общими ресурсами и служба хранилища
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Средства управления удаленным доступом
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Модуль удаленного доступа для Windows PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Графический интерфейс удаленного доступа и средства Command-Line
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Инструментари
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Средства диагностики лицензирования удаленный рабочий стол
</dt> <dd>

Добавлено

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Средства SNMP
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Средства многопользовательской активации
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Резервное копирование сервера
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Программы командной строки
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Поддержка рукописного ввода
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Распознавание рукописного текста
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Сервер Compact
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>подсистема WoW64 для платформа .NET Framework 2,0 и PowerShell
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>подсистема WoW64 для платформа .NET Framework 2,0
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>Подсистема WoW64 для PowerShell
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>подсистема WoW64 для платформа .NET Framework 3,0 и 3,5
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>Подсистема WoW64 для служб печати
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>Подсистема WoW64 для отказоустойчивой кластеризации
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>Подсистема WoW64 для редактора метода ввода
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>подсистема WoW64 для приложений на основе UNIX
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Возможности рабочего стола
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Графическая оболочка сервера
</dt> <dd>

Добавлено

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API и командлеты PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Установлен
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Службы WSUS
</dt> <dd>

Добавлено

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Консоль управления пользовательским интерфейсом
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Подключение WID
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>подсистема Windows PowerShell 2,0
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Веб-доступ
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>служба Desired State Configuration Windows PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>расширенная платформа .NET Framework 4,5
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Службы WCF
</dt> <dd>

Добавлено

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Активация по HTTP
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Активация очереди сообщений (MSMQ)
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Активация именованного канала
</dt> <dd>

Добавлено

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Активация по TCP
</dt> <dd>

Добавлено

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Совместное использование TCP-портов
</dt> <dd>

Добавлено

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5
</dt> <dd>

Добавлено

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Расширяемость .NET 4,5
</dt> <dd>

Добавлено

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess и VPN (RAS)
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Маршруты
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>служба хранилища Обслуживание
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Средства управления отказоустойчивыми кластерами
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>службы Active Directory Rights Management Инструментари
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Инициализация приложения
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Централизованная поддержка SSL-сертификатов
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Агент, поддерживающий утверждения
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Средства хоста удаленный рабочий стол сеансов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Протокол WebSocket
</dt> <dd>

больше не поддерживается

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Доступ к сети COM+
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Изменение имени файла и служб iSCSI
</dt> <dd>

Изменено на файловые службы

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Пользовательские интерфейсы и инфраструктура
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Сервер для NFS
</dt> <dd>

Добавлено

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Служба агента VSS файлового сервера
</dt> <dd>

Добавлено

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>сервер цели iSCSI
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Дедупликация данных
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Рабочие папки
</dt> <dd>

Удалено

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Основные службы
</dt> <dd>

Добавляется только для этой версии.

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>удаленный рабочий стол виртуальных графических элементов
</dt> <dd>

Добавлено только для этой версии

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Удаленный доступ
</dt> <dd>

Добавлено

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Службы UDDI
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows Системные диспетчер ресурсов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>диспетчер съемных служба хранилища
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>службы рукописного ввода
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Расширение IIS для WinRM
</dt> <dd>

Добавлено

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Консоль управления DirectAccess
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Фоновая интеллектуальная служба передачи (бит)
</dt> <dd>

Добавлено

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Средство просмотра XPS
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Биометрическая платформа
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Поддержка WoW64
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Интегрированная среда сценариев (ISE)
</dt> <dd>

Добавлено

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Служба репликации файлов
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache для сетевых файлов
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Рабочие папки
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>сервер распределенного сканирования
</dt> <dd>

Добавлено

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Служба FTP-публикаций
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Консоль управления FTP
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Служба FTP
</dt> <dd>

Добавлено

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Расширяемость FTP
</dt> <dd>

Добавлено

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Размещаемый в IIS веб-ядро
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>поддержка клиентов Windows 2000
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>веб-служба регистрации сертификатов
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>веб-служба политик регистрации сертификатов
</dt> <dd>

Добавлено

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Веб-приложение служб UDDI
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>База данных служб UDDI
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Расширения сервера приложений для .NET 4,0
</dt> <dd>

Добавлено

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Средства служб UDDI
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Служебные программы шифрование диска BitLocker Administration
</dt> <dd>

Добавлено

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Средства AD DS и AD LDS
</dt> <dd>

Больше не поддерживается

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Средства AD DS и AD LDS
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>центр администрирования Active Directory
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Модуль Active Directory для Windows PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Средства брокера подключение к удаленному рабочему столу
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>подсистема WoW64 для платформа .NET Framework 2,0 и Windows PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>подсистема WoW64 для платформа .NET Framework 2,0
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>Подсистема WoW64 для PowerShell
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>подсистема WoW64 для платформа .NET Framework 3,0 и 3,5
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>Подсистема WoW64 для служб печати
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>Подсистема WoW64 для отказоустойчивой кластеризации
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>Подсистема WoW64 для редактора метода ввода
</dt> <dd>

Добавлено

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>подсистема WoW64 для приложений на основе UNIX
</dt> <dd>

Добавлено

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Средство просмотра паролей восстановления BitLocker
</dt> <dd>

Добавлено

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Изменение имени службы печати и документов
</dt> <dd>

Именованные службы печати для этого выпуска

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Изменение имени службы удаленных рабочих столов
</dt> <dd>

Именованные службы терминалов в этом выпуске

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>изменение имени компонентов платформа .NET Framework 3.5.1
</dt> <dd>

в этом выпуске есть именованные функции платформа .NET Framework 3,0

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Изменение имени узла сеанса удаленный рабочий стол
</dt> <dd>

Именованный сервер терминалов в этом выпуске

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Изменение имени лицензирования удаленный рабочий стол
</dt> <dd>

Лицензирование служб терминалов в этом выпуске

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Изменение имени шлюза удаленный рабочий стол
</dt> <dd>

Именованный шлюз TS в этом выпуске

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Изменение имени компонента Service Broker подключение к удаленному рабочему столу
</dt> <dd>

Посредник сеансов служб терминалов в этом выпуске

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Изменение имени Веб-доступ удаленный рабочий стол
</dt> <dd>

Именованные Веб-доступ TS в этом выпуске

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>изменение имени платформа .NET Framework 3.5.1
</dt> <dd>

(220) в этом выпуске есть компоненты NET FX 3,0

(230) в этом выпуске имеется имя ядра сервера приложений

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Изменение имени инструментов AD DS
</dt> <dd>

В этом выпуске имеются именованные средства домен Active Directory Services

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Изменение имени AD LDS Snap-Ins и Command-Line средств
</dt> <dd>

В этом выпуске службы Active Directory облегченного доступа к каталогам средства с именем.

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Изменение имени инструментов службы печати и документов
</dt> <dd>

Средства именованных служб печати в этом выпуске

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Изменение имени инструментов службы удаленных рабочих столов
</dt> <dd>

В этом выпуске имеются именованные средства служб терминалов

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Изменение имени средств узла для удаленный рабочий стол сеансов
</dt> <dd>

В этом выпуске есть именованные средства сервера терминалов

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Изменение имени средств шлюза удаленный рабочий стол
</dt> <dd>

В этом выпуске есть именованные средства шлюза служб терминалов

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Изменение имени средств лицензирования удаленный рабочий стол
</dt> <dd>

Именованные средства лицензирования служб терминалов в этом выпуске

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Изменение имени AD DS Snap-Ins и Command-Line средств
</dt> <dd>

Средства контроллера домена Active Directory

</dd> </dl>

## <a name="examples"></a>Примеры

Следующий скрипт отображает имена всех компонентов сервера на компьютере с именем FABRIKAM. обратите внимание, что целевой компьютер должен работать под управлением Windows server 2008 или более поздней серверной операционной системы.


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Серверкомппров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

