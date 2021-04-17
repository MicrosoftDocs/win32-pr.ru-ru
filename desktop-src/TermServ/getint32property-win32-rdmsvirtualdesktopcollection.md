---
title: Метод GetInt32Property класса Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. аппаналисис. h)
description: Извлекает целочисленное свойство из коллекции виртуальных рабочих столов.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода GetInt32Property
- Службы удаленных рабочих столов метода GetInt32Property, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672507"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод GetInt32Property \_ класса Win32 рдмсвиртуалдесктопколлектион

Извлекает целочисленное свойство из коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Ключ, определяющий извлекаемое свойство.

</dd> <dt>

*Значение* \[ заполняет\]
</dt> <dd>

Целое число, получающее полученное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                                 |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                                   |
| Header<br/>                   | <dl> <dt>Microsoft. Diagnostics. аппаналисис. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





