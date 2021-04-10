---
description: Вызывает сохранение одного или нескольких свойств в контейнере свойств. Интерфейс Иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Метод Иитемпропертибаг:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144038"
---
# <a name="iitempropertybagwrite-method"></a>Метод Иитемпропертибаг:: Write

Вызывает сохранение одного или нескольких свойств в контейнере свойств. Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кпропертиес* \[ окне\]
</dt> <dd>

Число свойств для сохранения. Этот аргумент задает количество элементов в массивах по адресу *ппропбаг* и *сервер*.

</dd> <dt>

*ппропбаг* \[ окне\]
</dt> <dd>

Указатель на массив структур [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) , указывающий свойства, которые необходимо сохранить.

</dd> <dt>

*сервер* \[ окне\]
</dt> <dd>

Указатель на **вариант** , тип которого зависит от типа данных содержащихся в нем сведений о свойствах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.

Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпропертибаг**](iitempropertybag.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Распространяемые компоненты<br/>          | Поиск на рабочем столе Windows (WDS) 3,0<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иитемпропертибаг**](iitempropertybag.md)
</dt> </dl>

 

 




