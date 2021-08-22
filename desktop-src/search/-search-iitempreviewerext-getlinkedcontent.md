---
description: Допускает расширение к расширенному содержимому для свойства.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Метод Иитемпревиеверекст:: Жетлинкедконтент'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9b99d46d33ba66a9669d47021661b0a359fb2ca98d418735238e2baf3dc9e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094925"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>Метод Иитемпревиеверекст:: Жетлинкедконтент

Допускает расширение к расширенному содержимому для свойства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двконтекст* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Идентификатор контекста для операции. Переопределите *двконтекст* по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.

</dd> <dt>

*пвсзпроп* \[ окне\]
</dt> <dd>

Тип: **лпколестр**

Указатель на свойство связанного содержимого в виде строки в Юникоде.

</dd> <dt>

*пинфо* \[ out, retval\]
</dt> <dd>

Тип: **[ **линкинфо**](-search-linkinfo.md)\***

Получает указатель на структуру [**линкинфо**](-search-linkinfo.md) , в которой метод возвращает сведения о транзакции. *пинфо* не должен быть **пустым** указателем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.

для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие api: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структуру [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 3,0<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иитемпревиеверекст**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




