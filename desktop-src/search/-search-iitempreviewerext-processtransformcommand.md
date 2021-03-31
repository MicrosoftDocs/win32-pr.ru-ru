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
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896941"
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

Тип: **Variant \** _

Указатель на результирующий вариант. _pvarResult * не должен быть **пустым** указателем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) поддерживается только в Windows XP и windows Server 2003 и больше не должен использоваться.

Для предварительного просмотра вложений с помощью обработчика протоколов стороннего производителя на компьютерах под управлением Windows XP или Windows Server 2003 может потребоваться использовать интерфейс [**иитемпревиеверекст**](-search-iitempreviewerext.md) и следующие API: интерфейсы [**исеарчпротоколуи**](-search-isearchprotocolui.md), [**Иитемпропертибаг**](iitempropertybag.md) и [**исеарчитем**](-search-isearchitem.md) , структура [**линкинфо**](-search-linkinfo.md) и [**перечисление**](-search-linktype.md) типов ссылок.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |
| Распространяемые компоненты<br/>          | Поиск на рабочем столе Windows (WDS) 3,0<br/>          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иитемпревиеверекст**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




