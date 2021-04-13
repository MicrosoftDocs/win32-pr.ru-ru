---
title: Структура MPTHREAT_INFO (Мпклиент. h)
description: Содержит сведения об угрозе.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492630"
---
# <a name="mpthreat_info-structure"></a>\_Структура сведений о мпсреат

Содержит сведения об угрозе.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**среатид**
</dt> <dd>

Тип: **мпсреат \_ ID**

</dd> <dd>

Идентификатор угрозы. Верхний бит задан для выявления угроз, связанных с антивирусной программой.

</dd> <dt>

**детектионид**
</dt> <dd>

Тип: **GUID**

</dd> <dd>

Идентификатор обнаружения.

</dd> <dt>

**Name**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Имя угрозы.

</dd> <dt>

**среаттипе**
</dt> <dd>

Тип: **[ **мпсреат \_ тип**](mpthreat-type.md)**

</dd> <dd>

Тип угрозы. Используется для различения различных типов угроз, таких как известные плохие, неизвестные или известные хорошие проблемы. См. раздел [**\_ тип мпсреат**](mpthreat-type.md).

</dd> <dt>

**среаткритикалити**
</dt> <dd>

Тип: **[ **мпсреат \_ серьезность**](mpthreat-severity.md)**

</dd> <dd>

Критические угрозы. См. раздел [**мпсреат \_ Severity**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Тип: **[ **мпсреат \_ Category**](mpthreat-category.md)**

</dd> <dd>

Категория угроз, например Троян или троянская Keylogger. См [**. \_ раздел Категория мпсреат**](mpthreat-category.md).

</dd> <dt>

**среатшортдескриптионид**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Идентификатор краткого описания угрозы.

</dd> <dt>

**среатадвиседескриптионид**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

ИДЕНТИФИКАТОР описания рекомендации по угрозе.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Тип: **[ **\_ состояние мпсреат**](mpthreat-status.md)**

</dd> <dd>

Состояние угрозы, например обнаружено, очищено или помещено в карантин. См. сведения [**\_ о состоянии мпсреат**](mpthreat-status.md).

</dd> <dt>

**сугжестедактионкаунт**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Число предлагаемых действий в **сугжестедактионаррай**.

</dd> <dt>

**сугжестедактионаррай**
</dt> <dd>

Тип: **[**мпсреат \_ Action**](mpthreat-action.md) \[ MP \_ Max ( \_ рекомендации)\]**

</dd> <dd>

Массив предлагаемых действий. См. раздел [**\_ действие мпсреат**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Число ресурсов в **ресаурцелист**.

</dd> <dt>

**ресаурцелист**
</dt> <dd>

Введите: **пмпресаурце \_ info \** _

</dd> <dd>

Список ресурсов, определенных с помощью угрозы. См. раздел [_ *мпресаурце \_ info* *](mpresource-info.md).

</dd> <dt>

**среатстатустиме**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Время последнего изменения состояния угрозы.

</dd> <dt>

**среатстатускоде**
</dt> <dd>

Тип: **HRESULT**

</dd> <dd>

Код состояния, связанный с состоянием угрозы.

</dd> <dt>

**среатдетектион**
</dt> <dd>

Тип: **[ **\_ Обнаружение мпсреат**](mpthreat-detection.md)**

</dd> <dd>

Тип обнаружения угроз, например бетон, подозрительный или универсальный. См. раздел [**мпсреат \_ Detection**](mpthreat-detection.md).

</dd> <dt>

**куарантинегуид**
</dt> <dd>

Тип: **GUID**

</dd> <dd>

Идентификатор GUID карантина.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Тип: **[ **\_ состояние мпексекутион**](mpexecution-status.md)**

</dd> <dd>

Состояние выполнения угрозы, например неизвестная, заблокированная или активная. См. сведения [**\_ о состоянии мпексекутион**](mpexecution-status.md).

</dd> <dt>

**Data**
</dt> <dd>

Дополнительные сведения. Указатель на соответствующую структуру зависит от значения **среаттипе**.

<dl> <dt>

**пкновнбад**
</dt> <dd>

Тип: **пмпсреат \_ инфоекс не \_ используется**

</dd> <dd>

Если **среаттипе**  ==  **мпсреат \_ Type \_ кновнбад**. См. раздел [**мпсреат \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md).

</dd> <dt>

**пбехавиор**
</dt> <dd>

Тип: **пмпсреат \_ инфоекс \_ BEHAVIOR** .

</dd> <dd>

Когда   ==  **\_ \_ поведение типа мпсреат** среаттипе. См. раздел [**мпсреат \_ инфоекс \_ BEHAVIOR**](mpthreat-infoex-behavior.md).

</dd> <dt>

**pUnknown**
</dt> <dd>

Тип: **пмпсреат \_ инфоекс не \_ используется**

</dd> <dd>

Если   ==  **тип мпсреат \_ среаттипе \_ неизвестен**. См. раздел [**мпсреат \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md).

</dd> <dt>

**пкновнгуд**
</dt> <dd>

Тип: **пмпсреат \_ инфоекс не \_ используется**

</dd> <dd>

Если **среаттипе** = = мпсреат \_ Type \_ кновнгуд. См. раздел [**мпсреат \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md).

</dd> <dt>

**пнис**
</dt> <dd>

Тип: **пмпсреат \_ инфоекс \_ NIS** .

</dd> <dd>

При **среаттипе**  ==  **мпсреат \_ введите \_ NIS**. См. раздел [**мпсреат \_ инфоекс \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**Состояние**
</dt> <dd>

Тип: **[ **\_ состояние мпдетектион**](mpdetection-state.md)**

</dd> <dd>

Текущее состояние обнаружения. См. [**мпдетектион \_ State**](mpdetection-state.md).

</dd> <dt>

**детектионусер**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Пользователь, связанный с обнаружением, в формате "домен/пользователь".

</dd> <dt>

**детектионсаурце**
</dt> <dd>

Тип: **[ **мпсаурце**](mpsource.md)**

</dd> <dd>

Источник обнаружения. См. [**мпсаурце**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Имя процесса, связанное с обнаружением.

</dd> <dt>

**детектионоригин**
</dt> <dd>

Тип: **[ **мпдетектион \_ Origin**](mpdetection-origin.md)**

</dd> <dd>

Источник обнаружения, например локальный или сетевой. См. раздел [**мпдетектион \_ Origin**](mpdetection-origin.md).

</dd> <dt>

**reserved1**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Зарезервированные метаданные об обнаружении.

</dd> <dt>

**детектионтиме**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Время первоначального обнаружения.

</dd> <dt>

**приксекутионстатус**
</dt> <dd>

Тип: **[ **\_ состояние мпексекутион**](mpexecution-status.md)**

</dd> <dd>

Состояние выполнения непосредственно перед исправлением. См. сведения [**\_ о состоянии мпексекутион**](mpexecution-status.md).

</dd> <dt>

**ремедиатионтиме**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Возникло исправление времени.

</dd> <dt>

**постексекутионстатус**
</dt> <dd>

Тип: **[ **\_ состояние мпексекутион**](mpexecution-status.md)**

</dd> <dd>

Состояние выполнения после исправления. См. сведения [**\_ о состоянии мпексекутион**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Тип: **bool** .

</dd> <dd>

Значение true, если сбой исправления был критически важным.

</dd> <dt>

**нонкритикалреасон**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Причина сбоя исправления не является критической. В будущем это не обязательно будет поддерживаться.

</dd> <dt>

**ремедиатионусер**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Пользователь, запросивший исправление, в формате "домен/пользователь".

</dd> <dt>

**ремедиатионресаурцекаунт**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Число ресурсов в **ремедиатионресаурцелист**.

</dd> <dt>

**ремедиатионресаурцелист**
</dt> <dd>

Тип: **пмпресаурце \_ info \[ ремедиатионресаурцекаунт \]**

</dd> <dd>

Список ресурсов, которые завершились сбоем во время исправления. См [**. \_ сведения о мпресаурце**](mpresource-info.md).

</dd> <dt>

**фаилурересолвед**
</dt> <dd>

Тип: **bool** .

</dd> <dd>

Значение true, если ошибка исправления устранена. Контейнер будет перемещен в завершенное или дополнительное действие.

</dd> <dt>

**ресолведреасон**
</dt> <dd>

Тип: **[ **\_ Причина мпресолвед**](mpresolved-reason.md)**

</dd> <dd>

Причина разрешения ошибки исправления. Это причина, по которой обнаружение перешло с сбоя на дополнительное действие или завершено. См [**. \_ причину мпресолвед**](mpresolved-reason.md).

</dd> <dt>

**аддитионалактионс**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Требуются дополнительные действия.

</dd> <dt>

**ресолведактионс**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Любые дополнительные действия, которые были выполнены.

</dd> <dt>

**двсреатстатусфлаг**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Дополнительные сведения об обнаружении угроз.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мпфримемори**](mpfreememory.md)
</dt> <dt>

[**мпсреатенумерате**](mpthreatenumerate.md)
</dt> <dt>

[**мпсреаткуери**](mpthreatquery.md)
</dt> <dt>

[**\_источник мпдетектион**](mpdetection-origin.md)
</dt> <dt>

[**\_состояние мпдетектион**](mpdetection-state.md)
</dt> <dt>

[**\_состояние мпексекутион**](mpexecution-status.md)
</dt> <dt>

[**\_Причина мпресолвед**](mpresolved-reason.md)
</dt> <dt>

[**\_сведения о мпресаурце**](mpresource-info.md)
</dt> <dt>

[**мпсаурце**](mpsource.md)
</dt> <dt>

[**\_действие мпсреат**](mpthreat-action.md)
</dt> <dt>

[**\_Категория мпсреат**](mpthreat-category.md)
</dt> <dt>

[**\_Обнаружение мпсреат**](mpthreat-detection.md)
</dt> <dt>

[**\_поведение ИНФОЕКС \_ мпсреат**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**МПСРЕАТ \_ инфоекс \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**МПСРЕАТ \_ инфоекс не \_ используется**](mpthreat-infoex-unused.md)
</dt> <dt>

[**МПСРЕАТ \_ серьезность**](mpthreat-severity.md)
</dt> <dt>

[**\_состояние мпсреат**](mpthreat-status.md)
</dt> <dt>

[**\_тип мпсреат**](mpthreat-type.md)
</dt> </dl>

 

 





