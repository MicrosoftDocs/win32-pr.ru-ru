---
title: Перечисление Вмфлоппидискимажетипе (Впккоминтерфацес. h)
description: Указывает форматы дискет.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- Перечисление Вмфлоппидискимажетипе Virtual PC
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415504"
---
# <a name="vmfloppydiskimagetype-enumeration"></a>Перечисление Вмфлоппидискимажетипе

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает форматы дискет.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**Вмфлоппидискимаже \_ неизвестный**
</dt> <dd>

Неизвестный формат.

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**Вмфлоппидискимаже \_ ловденсити**
</dt> <dd>

Формат низкой плотности (720K).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**Вмфлоппидискимаже \_ хигхденсити**
</dt> <dd>

Формат высокой плотности (1,44 МБ).

</dd> <dt>

<span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**Вмфлоппидискимаже \_ DMF**
</dt> <dd>

Формат носителя распространения (1.68 МБ).

</dd> <dt>

<span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**Вмфлоппидискимаже \_ ловденситисинглесидед**
</dt> <dd>

Односторонняя формат низкой плотности.

</dd> <dt>

<span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**Вмфлоппидискимаже \_ медиумденсити**
</dt> <dd>

Формат средней плотности (1,2 МБ).

</dd> <dt>

<span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**Вмфлоппидискимаже \_ хигхденситимсс**
</dt> <dd>

Высокоплотный размер сектора (MSS), используемый расширенным форматом распределения (Xdf-).

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

[**Ивмвиртуалпк:: Креатефлоппидискимаже**](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[**Ивмвиртуалпк:: Жетфлоппидискимажетипе**](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

