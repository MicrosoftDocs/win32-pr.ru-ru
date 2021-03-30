---
description: Метод Жетпровидеркардид извлекает идентификатор (GUID) основного поставщика услуг для указанной смарт-карты.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Метод Искарддатабасе:: Жетпровидеркардид (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816792"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>Метод Искарддатабасе:: Жетпровидеркардид

\[Метод **жетпровидеркардид** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **жетпровидеркардид** извлекает идентификатор (GUID) [*основного поставщика услуг*](../secgloss/p-gly.md) для указанной [*смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстркарднаме* \[ окне\]
</dt> <dd>

Имя смарт-карты.

</dd> <dt>

*ппгуидпровидерид* \[ заполняет\]
</dt> <dd>

Указатель на идентификатор первичного поставщика служб (GUID) в случае успешного выполнения; **Null** , если операция завершилась ошибкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                              |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппгуидпровидерид* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                                  |



 

## <a name="remarks"></a>Комментарии

Чтобы получить список интерфейсов смарт-карты, вызовите [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md).

Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md), [*читатели*](../secgloss/r-gly.md) и [*группы читателей*](../secgloss/r-gly.md) вызывают [**листкардс**](iscarddatabase-listcards.md), [**листреадерс**](iscarddatabase-listreaders.md)и [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано получение идентификатора первичного поставщика услуг для указанной смарт-карты.


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
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

[**искарддатабасе**](iscarddatabase.md)
</dt> <dt>

[**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**листреадерграупс**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**листреадерс**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
