---
description: Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств. интерфейс иитемпропертибаг поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.
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
ms.openlocfilehash: 7a69ceff2236a101f18ee06b4a87dd60e35ca69e73fdeb085232f102f8450d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863093"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Метод Иитемпропертибаг:: GetPropertyInfo

Возвращает сведения, необходимые для чтения или сохранения свойств в контейнере свойств. интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.

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

## <a name="remarks"></a>Remarks

интерфейс [**иитемпропертибаг**](iitempropertybag.md) поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.

для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпропертибаг**](iitempropertybag.md) и следующие api: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**иитемпревиеверекст**](-search-iitempreviewerext.md) и [**исеарчитем**](-search-isearchitem.md) , структуры [**линкинфо**](-search-linkinfo.md) и [**итемпроп**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 3,0<br/>          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иитемпропертибаг**](iitempropertybag.md)
</dt> </dl>

 

 




