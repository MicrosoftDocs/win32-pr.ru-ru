---
description: Создает интерфейс Искардверифи.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: 'Метод Искардманаже:: Креатечверификатион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 312fc18be42ccc7ba35a0d0a6288637bd92cd0f10a855dc95c457329c69cd7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922771"
---
# <a name="iscardmanagecreatechverification-method"></a>Метод Искардманаже:: Креатечверификатион

\[Метод **креатечверификатион** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **креатечверификатион** создает интерфейс [**искардверифи**](iscardverify.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппискардверифи* \[ заполняет\]
</dt> <dd>

Возвращен указатель на созданный интерфейс [**искардверифи**](iscardverify.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *ппискардверифи* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппискардверифи* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                                |



 

## <a name="remarks"></a>Remarks

Список всех методов, определенных этим интерфейсом, см. в разделе [**искардманаже**](iscardmanage.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардманаже**](iscardmanage.md)
</dt> <dt>

[**искардверифи**](iscardverify.md)
</dt> </dl>

 

 
