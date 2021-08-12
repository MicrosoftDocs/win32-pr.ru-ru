---
title: Структура _VIDEOINFOHEADER
description: '\_Структура видеоинфохеадер содержит сведения о видеопотоке и включает \_ структуру битмапинфохеадер, определяющую формат отдельного кадра.'
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b00c641f0fb9a9f68217de8a21a732b4b45a8e4417104be981ffd90161f7340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586804"
---
# <a name="_videoinfoheader-structure"></a>\_Структура ВИДЕОИНФОХЕАДЕР

Структура **\_ видеоинфохеадер** содержит сведения о видеопотоке и включает структуру **\_ битмапинфохеадер** , определяющую формат отдельного кадра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**рксаурце**
</dt> <dd>

Структура **Rect** , указывающая исходное видеоокно.

</dd> <dt>

**рктаржет**
</dt> <dd>

Структура **Rect** , указывающая целевое окно видео.

</dd> <dt>

**двбитрате**
</dt> <dd>

Значение **типа DWORD** , указывающее приблизительную скорость передачи данных видеопотока в битах в секунду.

</dd> <dt>

**двбитерроррате**
</dt> <dd>

Значение **типа DWORD** , указывающее частоту ошибок данных потока видео в битах в секунду.

</dd> <dt>

**авгтимеперфраме**
</dt> <dd>

**Справочные материалы \_ Значение времени** , указывающее среднее время показа видеокадра (в 100-наносекундных единицах).

</dd> <dt>

**бмихеадер**
</dt> <dd>

Структура Win32 **\_ битмапинфохеадер** , которая содержит сведения о цвете и измерении для растрового изображения видео.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_битмапинфохеадер**](-bitmapinfoheader.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





