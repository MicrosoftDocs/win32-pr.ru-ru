---
description: Вызывает считывание одного или нескольких свойств из контейнера свойств. интерфейс иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: 'Метод Иитемпропертибаг:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c04cf34720871b1254f16822a090f48f8d68aaeb82398744d5139486fb6dd2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226609"
---
# <a name="iitempropertybagread-method"></a>Метод Иитемпропертибаг:: Read

Вызывает считывание одного или нескольких свойств из контейнера свойств. интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кпропертиес* \[ окне\]
</dt> <dd>

Число свойств для чтения. Этот аргумент задает количество элементов в массивах по *ппропбаг*, *сервер* и *фреррор*.

</dd> <dt>

*ппропбаг* \[ окне\]
</dt> <dd>

Указатель на массив структур [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) , указывающих запрашиваемые свойства.

</dd> <dt>

*сервер* \[ заполняет\]
</dt> <dd>

Получает указатель, возвращающий массив **вариативных** структур, которые получают значения свойств.

</dd> <dt>

*фреррор* \[ заполняет\]
</dt> <dd>

Указатель на массив значений **HRESULT** , которые получают результат каждого прочитанного свойства. В этом массиве должно быть по крайней мере *кпропертиес* элементов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.

для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпропертибаг**](iitempropertybag.md) и следующие api: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 3,0<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иитемпропертибаг**](iitempropertybag.md)
</dt> </dl>

 

 




