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
ms.openlocfilehash: 7c68d1bb7bfd41293521319cf20d0f6c5afdc73543fa0cd8b13366bfcbeb77a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998514"
---
# <a name="vmharddisktype-enumeration"></a>Перечисление Вмхарддисктипе

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмхарддиск**](ivmharddisk.md)
</dt> </dl>

 

