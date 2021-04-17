---
description: Возвращает связанную часть тела для внедрения в выходной поток MHTML.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: 'Метод Иитемпревиеверекст:: Жетрелатедпарт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 281d91b1679b2a944996bb1c85060d16c4e0b966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710923"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>Метод Иитемпревиеверекст:: Жетрелатедпарт

Возвращает связанную часть тела для внедрения в выходной поток MHTML.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двконтекст* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Идентификатор контекста для операции. Переопределите **двконтекст** по умолчанию, чтобы задать для идентификатора контекста значение, выбранное вами.

</dd> <dt>

*пвсзпроп* \[ окне\]
</dt> <dd>

Тип: **лпколестр**

Указатель на свойство связанного содержимого в виде строки в Юникоде.

</dd> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Длинное целое число без знака, содержащее Отсчитываемый от нуля индекс связанной части тела.

</dd> <dt>

*пинфо* \[ out, retval\]
</dt> <dd>

Тип: **[**линкинфо**](-search-linkinfo.md) \** _

Получает указатель на структуру [_ *линкинфо* *](-search-linkinfo.md) , в которой метод возвращает сведения о транзакции. *пинфо* не должен быть **пустым** указателем.

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

 

 




