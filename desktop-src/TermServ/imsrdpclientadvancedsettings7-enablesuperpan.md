---
title: IMsRdpClientAdvancedSettings7 Енаблесуперпан, свойство
description: Указывает или получает логическое значение, указывающее, включен ли параметр Суперпан.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблесуперпан
- Службы удаленных рабочих столов свойства Енаблесуперпан, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Енаблесуперпан
- Службы удаленных рабочих столов свойства Енаблесуперпан, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Енаблесуперпан
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802752"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a>Свойство IMsRdpClientAdvancedSettings7:: Енаблесуперпан

Указывает или получает логическое значение, указывающее, включен ли параметр Суперпан. Суперпан — это функция, позволяющая пользователю легко перемещаться по удаленному рабочему столу в полноэкранном режиме, если размеры удаленного рабочего стола больше, чем размеры текущего окна клиента. Вместо использования полос прокрутки для навигации по рабочему столу пользователь может указать границу окна, и удаленный рабочий стол будет автоматически прокручиваться в этом направлении. Суперпан не поддерживает более одного монитора.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a>Значение свойства

Значение **типа Variant \_ bool** , указывающее, включен ли суперпан. Значение **Variant \_ true** указывает, что суперпан включен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





