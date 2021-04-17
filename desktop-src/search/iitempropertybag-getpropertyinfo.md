---
description: Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств. Интерфейс Иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Метод Иитемпропертибаг:: GetPropertyInfo'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710903"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Метод Иитемпропертибаг:: GetPropertyInfo

Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств. Интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ипроперти* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс первого свойства, для которого запрашиваются сведения.

</dd> <dt>

*кпропертиес* \[ окне\]
</dt> <dd>

Число свойств, для которых необходимо получить сведения. Этот аргумент задает количество элементов массива в *ппропбаг*.

</dd> <dt>

*ппропбаг* \[ заполняет\]
</dt> <dd>

Указатель на массив структур [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) , которые получают сведения о свойствах.

</dd> <dt>

*пкпропертиес* \[ заполняет\]
</dt> <dd>

Получает указатель на переменную **ulong** , которая получает количество свойств, для которых была получена информация.

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

 

 




