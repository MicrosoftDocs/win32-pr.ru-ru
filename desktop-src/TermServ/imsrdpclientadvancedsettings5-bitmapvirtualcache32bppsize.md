---
title: IMsRdpClientAdvancedSettings5 BitmapVirtualCache32BppSize, свойство
description: Задает или получает размер файла виртуального кэша для точечных рисунков 32 бит на пиксель (бит в пикселах).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство BitmapVirtualCache32BppSize
- Службы удаленных рабочих столов свойства BitmapVirtualCache32BppSize, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415173"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a>Свойство IMsRdpClientAdvancedSettings5:: BitmapVirtualCache32BppSize

Задает или получает размер файла виртуального кэша для точечных рисунков 32 бит на пиксель (бит в пикселах).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a>Значение свойства

Задает размер файла виртуального кэша для точечных рисунков 32 бит/с в мегабайтах (МБ). Максимальное значение — 48 МБ.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 определяется как FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





