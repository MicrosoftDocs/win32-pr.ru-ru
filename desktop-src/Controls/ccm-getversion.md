---
title: Сообщение CCM_GETVERSION (Коммктрл. h)
description: Возвращает номер версии элемента управления, заданного последним \_ сообщением CCM сетверсион.
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- элементы управления Windows сообщений CCM_GETVERSION
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ad49ebb00d5d57555bb07be1bcf78ab97115ada43e18a7f81cda93e29fa1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320264"
---
# <a name="ccm_getversion-message"></a>Сообщение CCM для \_ версии

Возвращает номер версии элемента управления, заданного последним сообщением [**CCM \_ сетверсион**](ccm-setversion.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает номер версии, заданный последним сообщением [**CCM \_ сетверсион**](ccm-setversion.md) . Если такое сообщение не было отправлено, оно возвращает ноль.

## <a name="remarks"></a>Remarks

Это сообщение не возвращает версию библиотеки DLL. Сведения об использовании [**дллжетверсион**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) для получения текущей версии DLL см. в статье [версии оболочки](common-control-versions.md) .

> [!Note]  
> Номер версии задается для каждого элемента управления и может отличаться для всех элементов управления.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

