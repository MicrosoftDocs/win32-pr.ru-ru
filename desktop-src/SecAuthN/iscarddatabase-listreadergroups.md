---
description: Метод Листреадерграупс извлекает имена групп читателей, зарегистрированных в базе данных смарт-карты.
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'Метод Искарддатабасе:: Листреадерграупс (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 00753b0ca3964dc5a35e26db0eec2aedda4d2511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145265"
---
# <a name="iscarddatabaselistreadergroups-method"></a>Метод Искарддатабасе:: Листреадерграупс

\[Метод **листреадерграупс** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **листреадерграупс** извлекает имена [*групп читателей*](../secgloss/r-gly.md) , зарегистрированных в базе данных смарт-карты.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*LocaleID* \[ окне\]
</dt> <dd>

ИДЕНТИФИКАТОР локализации языка.

</dd> <dt>

*ппреадерграупс* \[ заполняет\]
</dt> <dd>

Указатель на массив SAFEARRAY, содержащий имена групп считывателей смарт-карт, которые удовлетворяют параметрам поиска в случае успеха. **Значение NULL** , если операция завершилась ошибкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                            |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппреадерграупс* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                                |



 

## <a name="remarks"></a>Комментарии

Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md) или [*модули чтения*](../secgloss/r-gly.md), вызовите [**листкардс**](iscarddatabase-listcards.md) или [**листреадерс**](iscarddatabase-listreaders.md) соответственно.

Получение [*первичного поставщика услуг*](../secgloss/p-gly.md) или интерфейсов конкретного адаптера [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md) или [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано получение имен групп читателей, зарегистрированных в базе данных смарт-карты.


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Скардмгр. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардмгр. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетпровидеркардид**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**искарддатабасе**](iscarddatabase.md)
</dt> <dt>

[**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**листреадерс**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
