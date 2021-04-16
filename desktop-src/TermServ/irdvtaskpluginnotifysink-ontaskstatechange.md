---
title: Ирдвтаскплугиннотифисинк Онтаскстатечанже, метод
description: Используется для уведомления агента активации о том, что состояние задачи изменилось.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онтаскстатечанже
- Службы удаленных рабочих столов метода Онтаскстатечанже, интерфейс Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, метод Онтаскстатечанже
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672863"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>Метод Ирдвтаскплугиннотифисинк:: Онтаскстатечанже

Используется для уведомления агента активации о том, что состояние задачи изменилось.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*bstrIdentifier* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Идентификатор задачи. Это идентификатор, передаваемый методу [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*состояние* \[ окне\]
</dt> <dd>

Тип: **[ **RDV \_ задача \_ состояние**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Значение перечисления [**\_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , которое указывает новое состояние задачи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Windows 7 Корпоративная<br/>   |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_состояние задачи \_ RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**ирдвтаскплугиннотифисинк**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





