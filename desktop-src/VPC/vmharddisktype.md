---
title: Перечисление Вмхарддисктипе (Впккоминтерфацес. h)
description: Указывает тип образа жесткого диска.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- Перечисление Вмхарддисктипе Virtual PC
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691888"
---
# <a name="vmharddisktype-enumeration"></a>Перечисление Вмхарддисктипе

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает тип образа жесткого диска.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**Вмдисктипе \_ dynamic**
</dt> <dd>

Динамически расширяемый образ жесткого диска.

</dd> <dt>

<span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**Вмдисктипе \_ FixedSize**
</dt> <dd>

Образ жесткого диска фиксированного размера.

</dd> <dt>

<span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**\_разностное вмдисктипе**
</dt> <dd>

Образ разностного жесткого диска.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмхарддиск**](ivmharddisk.md)
</dt> </dl>

 

