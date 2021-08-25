---
description: Включает это самонастраивающийся устройство.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Enable, метод класса Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a5c0db362431a2dac479077861a33a46f296b71f4b570a43a963292ac8446b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879104"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a>Enable, метод класса Win32 \_ пнпентити

Включает это самонастраивающийся устройство.

## <a name="syntax"></a>Синтаксис


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ребутнидед* \[ заполняет\]
</dt> <dd>

Необходимость перезагрузки.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Пнпентити Win32**](win32-pnpentity.md)
</dt> </dl>

 

 




