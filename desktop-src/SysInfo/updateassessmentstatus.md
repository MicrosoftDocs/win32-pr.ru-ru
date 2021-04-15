---
description: Описание обновления операционной системы на устройстве.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Перечисление Упдатеассессментстатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662540"
---
# <a name="updateassessmentstatus-enumeration"></a>Перечисление Упдатеассессментстатус

Описание обновления операционной системы на устройстве. **Упдатеассессментстатус** используется структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) и [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) в членах **ассессментфоркуррент**, **ассессментфоруптодате** и **securityStatus** . Возвращается ровно одна константа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**Упдатеассессментстатус \_ Последняя версия**
</dt> <dd>

Этот результат в **ассессментфоркуррент** означает, что устройство находится в последней версии обновления компонентов и качества, доступном для этого устройства. В **ассессментфоруптодате** этот результат означает, что устройство находится в последнем обновлении для выпуска Windows, на котором он работает.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**Упдатеассессментстатус \_ Нотлатестсофтрестриктион**
</dt> <dd>

Последнее обновление компонента не было установлено из-за необратимого ограничения. Если в обновление было включено мягкое ограничение, обновление не будет установлено автоматически. пользователь должен самостоятельно инициировать скачивание в рамках обновления. Это состояние применяется только к **ассессментфоркуррент**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**Упдатеассессментстатус \_ Нотлатессардрестриктион**
</dt> <dd>

Последнее обновление компонента не было установлено в связи с жестким ограничением. Если в обновление было размещено жесткое ограничение, обновление не применяется к устройству. Это состояние применяется только к **ассессментфоркуррент**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**Упдатеассессментстатус \_ Нотлатестендофсуппорт**
</dt> <dd>

Устройство не находится в последнем обновлении, так как обновление компонентов устройства больше не поддерживается корпорацией Майкрософт. Когда корпорация Майкрософт прекращает поддержку выпуска компонентов, это состояние будет возвращено как для **ассессментфоркуррент** , так и для **ассессментфоруптодате**.

> [!Note]  
> Когда возвращается **упдатеассессментстатус \_ Нотлатестендофсуппорт** , **упдатеимпактлевел** оценки всегда имеет значение **\_ High упдатеимпактлевел**.

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**Упдатеассессментстатус \_ НотлатестсервиЦингтраин**
</dt> <dd>

Устройство не находится в новейшем обновлении компонентов, так как обслуживание устройства обработает ограничение на обновление до последнего обновления компонента. Например, если устройство находится на Current Branch for Business (CBB) и для Current Branch (CB) выпущено новое обновление, будет возвращено следующее. Это состояние применяется только к **ассессментфоркуррент**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**Упдатеассессментстатус \_ Нотлатестдеферредфеатуре**
</dt> <dd>

Последнее обновление компонента не было установлено из-за политики отсрочки для обновления бизнес-компонентов на устройстве Центр обновления Windows. При определении **дайсаутофдате** учитываются политики отсрочки. **дайсаутофдате** не начнет увеличиваться до тех пор, пока не истечет период отсрочки. Это состояние применяется только к **ассессментфоркуррент**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**Упдатеассессментстатус \_ Нотлатестдеферредкуалити**
</dt> <dd>

Это устройство не включено в Последнее обновление, так как для политики отсрочки обновления качества бизнеса на устройстве Центр обновления Windows. При определении **дайсаутофдате** учитываются политики отсрочки. **дайсаутофдате** не начнет увеличиваться до тех пор, пока не истечет период отсрочки.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**Упдатеассессментстатус \_ Нотлатестпауседфеатуре**
</dt> <dd>

Устройство не находится на последнем обновлении компонентов из-за приостановки обновления компонентов. Является ли устройство приостановленным, не учитывается при вычислении **дайсаутофдате**. Это состояние применяется только к **ассессментфоркуррент**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**Упдатеассессментстатус \_ Нотлатестпауседкуалити**
</dt> <dd>

Устройство не находится в последнем обновлении, так как оно приостановило обновление качества. Является ли устройство приостановленным, не учитывается при вычислении **дайсаутофдате**. **дайсаутофдате** не определяет, приостанавливается ли устройство к его вычислению.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**Упдатеассессментстатус \_ Нотлатестманажед**
</dt> <dd>

Устройство не находится в последнем обновлении, так как утверждение обновлений не выполняется с помощью Центр обновления Windows.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**Упдатеассессментстатус \_ Нотлатестункновн**
</dt> <dd>

Устройство не находится в последнем обновлении из-за причины, которая не может быть определена оценкой.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**Упдатеассессментстатус \_ Нотлатесттаржетедверсион**
</dt> <dd>

Устройство не находится в последнем обновлении компонентов из-за политики Центр обновления Windows на устройстве для целевой версии. Эта политика позволяет сохранить устройство в целевой версии выпуска.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление чаще всего используется с структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) и [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , которые, в свою очередь, используются с методом [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) для [**иваасассессор**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>Ваасапи. idl</dt> </dl> |



 

 




