---
description: Разрешает обработку команды преобразования, обнаруженной в шаблоне предварительной версии.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: 'Иитемпревиеверекст: метод:P Роцесстрансформкомманд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: f93d4be0bf9491c4fd2f6074c00692d6f634704ec820a34baeb4f1d52343c36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969782"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>Иитемпревиеверекст: метод:P Роцесстрансформкомманд

Разрешает обработку команды преобразования, обнаруженной в шаблоне предварительной версии.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двконтекст* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Идентификатор контекста для операции. Переопределите *двконтекст* по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.

</dd> <dt>

*pwszName* \[ окне\]
</dt> <dd>

Тип: **лпколестр**

Указатель на имя команды преобразования в виде строки Юникода.

</dd> <dt>

*пвсзарг* \[ окне\]
</dt> <dd>

Тип: **лпколестр**

Указатель на аргумент в виде строки в Юникоде.

</dd> <dt>

*пварресулт* \[ out, retval\]
</dt> <dd>

Тип: **Variant \***

Указатель на результирующий вариант. *пварресулт* не должен быть **пустым** указателем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и Windows Server 2003 и больше не должен использоваться.

для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие api: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структуру [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Распространяемые компоненты<br/>          | Windows Поиск на рабочем столе (WDS) 3,0<br/>          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иитемпревиеверекст**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




