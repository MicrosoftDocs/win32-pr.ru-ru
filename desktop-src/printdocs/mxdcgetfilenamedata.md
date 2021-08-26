---
description: Структура МКСДК \_ Get \_ filename \_ Data \_ T содержит полный путь и имя выходного файла конвертера документов Microsoft XPS (мксдк).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Структура MXDC_GET_FILENAME_DATA_T (Мксдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ef0b29590b4a9080e943fae5c3e78fb18a99232a2a531a80b63b303b28c2bea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948344"
---
# <a name="mxdc_get_filename_data_t-structure"></a>МКСДК \_ получить \_ \_ структуру данных имени файла \_ T

Структура **мксдк \_ Get \_ filename \_ Data \_ T** содержит полный путь и имя выходного файла конвертера документов Microsoft XPS (мксдк).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбаутпут**
</dt> <dd>

Размер выходного буфера **всздата**.

</dd> <dt>

**всздата**
</dt> <dd>

Полный путь и имя выходного файла.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура возвращается функцией [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , когда она вызывается с помощью escape-последовательности [**мксдк \_**](mxdc-escape.md) , а структура [**Escape- \_ \_ заголовка \_ мксдк**](mxdcescapeheader.md) , которая передается в параметр *лпсзиндата* , **имеет значение** **мксдкоп \_ Get \_ filename**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                    |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Мксдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[Escape-функции принтера GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**Escape-МКСДК \_**](mxdc-escape.md)
</dt> </dl>

 

