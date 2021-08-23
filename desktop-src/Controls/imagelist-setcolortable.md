---
title: Функция ImageList_SetColorTable
description: Задает таблицу цветов для списка изображений.
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTableные элементы управления Windows функции
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412242"
---
# <a name="imagelist_setcolortable-function"></a>Сетколортабле ImageList, \_ функция

Задает таблицу цветов для списка изображений.

## <a name="syntax"></a>Синтаксис


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*химл* \[ окне\]
</dt> <dd>

Тип: **химажелист**

Маркер списка изображений.

</dd> <dt>

*Запуск* \[ окне\]
</dt> <dd>

Тип: **int**

Индекс таблицы цветов, начинающийся с нуля, указывающий первую заданную запись в таблице цветов.

</dd> <dt>

*Len* \[ окне\]
</dt> <dd>

Тип: **int**

Число заданных записей в таблице цветов.

</dd> <dt>

*пргб* \[ окне\]
</dt> <dd>

Тип: **[ **ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

Указатель на массив [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) структур *Len* , содержащий новые сведения о цвете для таблицы цветов DIB.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **int**

Если функция выполнена, возвращается число записей в таблице цветов, заданных функцией. Если функция завершается ошибкой, возвращаемое значение меньше или равно нулю.

## <a name="remarks"></a>Remarks

Только списки изображений, созданные с помощью флага [**ILC \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) или [**ILC \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , имеют таблицы цветов. Цветовая таблица такого списка изображений обычно устанавливается автоматически путем копирования таблицы цветов первого изображения, добавленного в список (например, с помощью функции [**\_ Add ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) ), если это изображение имеет формат DIB. Если первое изображение, добавленное в список изображений, не является DIB, то таблица цветов палитры полутонового изображения используется для **ILC \_ COLOR8** , а таблица цветов VGA используется для **ILC \_ COLOR4**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (версия 3,51 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Таблица цветов](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

