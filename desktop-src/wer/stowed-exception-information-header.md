---
title: Структура STOWED_EXCEPTION_INFORMATION_HEADER
description: Содержит сведения, определяющие родительскую структуру.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER структуры отчеты об ошибках Windows
- PSTOWED_EXCEPTION_INFORMATION_HEADER отчеты об ошибках Windows указателя на структуру
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071932"
---
# <a name="stowed_exception_information_header-structure"></a>\_ \_ Структура заголовка сведений об ИСКЛЮЧЕНии заполнения \_

Содержит сведения, определяющие родительскую структуру.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Размер родительской структуры в байтах.

</dd> <dt>

**Образец**
</dt> <dd>

Тип: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

32-разрядное значение, указывающее сигнатуру родительской структуры.



| Значение                                                                                                                                                                                                                                                                                                            | Значение                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**Заполнения \_ \_Сведения об исключении \_ v1, \_ подпись**</dt> <dt>"SE01"</dt> </dl> | Это значение указывает, что родительским объектом является структура **заполнения \_ исключения \_ \_ v1** .<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**Заполнения \_ \_Сведения об исключении \_ v2 \_ сигнатура**</dt> <dt>"SE02"</dt> </dl> | Это значение указывает, что родительским объектом является структура [**заполнения \_ исключения \_ \_ v2**](stowed-exception-information-v2.md) .<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

[**Заполнения \_ Заголовок сведений об ИСКЛЮЧЕНии \_ \_ v2**](stowed-exception-information-v2.md) и заполнения в настоящее время не определен в заголовке, который является общедоступным, поэтому необходимо определить их в исходном коде, прежде чем использовать их. **\_ \_ \_**

Структура **\_ \_ сведений об исключении \_ заполнения** версии 1 идентична этой структуре, за исключением того, что она не содержит членов **нестедексцептионтипе** и **нестедексцептион** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                            |
| Header<br/>                   | <dl> <dt>Нет</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Сведения об исключении заполнения \_ \_ v2**](stowed-exception-information-v2.md)
</dt> </dl>

 

