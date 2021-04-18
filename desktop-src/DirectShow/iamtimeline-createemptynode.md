---
description: Метод Креатимптиноде создает новый объект Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'Метод Иамтимелине:: Креатимптиноде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675292"
---
# <a name="iamtimelinecreateemptynode-method"></a>Метод Иамтимелине:: Креатимптиноде

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`CreateEmptyNode`Метод создает новый объект временной шкалы.

Этот метод используется для создания объектов временной шкалы, а не функции **CoCreateInstance** , поскольку этот метод выполняет важные процедуры инициализации. Каждый объект, созданный этим методом, поддерживает по крайней мере интерфейс [**иамтимелинеобж**](iamtimelineobj.md) , а также другие интерфейсы, относящиеся к этому типу объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппобж* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) нового объекта.

</dd> <dt>

*Тип* 
</dt> <dd>

Элемент перечисляемого типа " [**\_ основной \_ тип временной шкалы**](timeline-major-type.md) ", указывающий тип создаваемого объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Не добавляйте новый объект в другой экземпляр временной шкалы. Каждый объект на временной шкале должен быть создан этой временной шкалой.

Если метод завершается успешно, интерфейс [**иамтимелинеобж**](iamtimelineobj.md) , который он возвращает, имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




