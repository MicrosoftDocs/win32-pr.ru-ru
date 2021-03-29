---
description: '\_Структура фильтра амовиесетуп содержит сведения для регистрации фильтра.'
ms.assetid: 72e58f33-e480-4b32-b3d5-8f6c8eb2d5a3
title: Структура AMOVIESETUP_FILTER (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMOVIESETUP_FILTER
api_type:
- HeaderDef
api_location:
- combase.h
ms.openlocfilehash: 55a225185733a822591d8f93c2eca3674d51a340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657838"
---
# <a name="amoviesetup_filter-structure"></a>\_Структура фильтра амовиесетуп

Структура **\_ фильтра амовиесетуп** содержит сведения для регистрации фильтра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _AMOVIESETUP_FILTER {
  const  CLSID           *clsID;
  const  WCHAR           *strName;
  DWORD                  dwMerit;
  UINT                   nPins;
  const  AMOVIESETUP_PIN *lpPin;
} AMOVIESETUP_FILTER, *PAMOVIESETUP_FILTER, *FAR LPAMOVIESETUP_FILTER;
```



## <a name="members"></a>Члены

<dl> <dt>

**Этому**
</dt> <dd>

Идентификатор класса фильтра.

</dd> <dt>

**strName**
</dt> <dd>

Имя фильтра.

</dd> <dt>

**двмерит**
</dt> <dd>

Отфильтровать. Используется интерфейсом [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) при создании графа фильтра. Список значений для получения списка недопустимых данных [см. в](merit.md)разделе.

</dd> <dt>

**нпинс**
</dt> <dd>

Число элементов в массиве *лппин* . Если *лппин* имеет **значение NULL**, присвойте этому элементу значение 0.

</dd> <dt>

**лппин**
</dt> <dd>

Указатель на массив [**амовиесетупных структур \_ закрепления**](amoviesetup-pin.md) размера *нпинс*. Каждый член этого массива описывает ПИН-код фильтра.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сведения об использовании этой структуры см. [в разделе Регистрация фильтров DirectShow](how-to-register-directshow-filters.md). Используйте эту структуру только для фильтров, зарегистрированных в категории фильтра по умолчанию (CLSID \_ легациамфилтеркатегори). Чтобы зарегистрировать фильтр в другой категории, используйте метод [**IFilterMapper2:: регистерфилтер**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) , как описано в разделе [Реализация DllRegisterServer](implementing-dllregisterserver.md).

> [!Note]  
> Файл заголовка комбасе. h предоставляется [базовыми классами DirectShow](directshow-base-classes.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Комбасе. h (включение Streams. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DirectShow](directshow-structures.md)
</dt> </dl>

 

 




