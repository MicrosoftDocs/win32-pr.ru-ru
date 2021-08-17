---
title: IMsRdpClientAdvancedSettings6 Релативемаусемоде, свойство
description: Указывает, следует ли использовать относительный режим для мыши.
ms.assetid: 29ae9575-ce60-4999-9601-18413ae739e6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Релативемаусемоде
- Службы удаленных рабочих столов свойства Релативемаусемоде, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Релативемаусемоде
- Службы удаленных рабочих столов свойства Релативемаусемоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Релативемаусемоде
- Службы удаленных рабочих столов свойства Релативемаусемоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Релативемаусемоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.RelativeMouseMode
- IMsRdpClientAdvancedSettings6.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings6.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.RelativeMouseMode
- IMsRdpClientAdvancedSettings7.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings7.put_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.RelativeMouseMode
- IMsRdpClientAdvancedSettings8.get_RelativeMouseMode
- IMsRdpClientAdvancedSettings8.put_RelativeMouseMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfe0551cf02f94f3494fde5ebf49ffb60c2bd4a966db1efb5f0dfeb3bd9e4bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138817"
---
# <a name="imsrdpclientadvancedsettings6relativemousemode-property"></a>Свойство IMsRdpClientAdvancedSettings6:: Релативемаусемоде

Указывает, следует ли использовать относительный режим для мыши. Содержит **вариант \_ true** , если мышь находится в относительном режиме, или **вариант \_ false** , если мышь находится в абсолютном режиме.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RelativeMouseMode(
  [in]          VARIANT_BOOL fRelativeMouseMode
);

HRESULT get_RelativeMouseMode(
  [out, retval] VARIANT_BOOL *pfRelativeMouseMode
);
```



## <a name="property-value"></a>Значение свойства

Содержит новое значение свойства.

## <a name="remarks"></a>Remarks

режим мыши показывает, как элемент управления ActiveX вычисляет координаты мыши, которые она отправляет на сервер узла сеансов удаленный рабочий стол. когда мышь находится в относительном режиме, элемент управления ActiveX вычисляет координаты мыши относительно последней положения мыши. когда мышь находится в абсолютном режиме, элемент управления ActiveX вычисляет координаты мыши относительно рабочего стола сервера узла сеансов удаленных рабочих столов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1)<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





