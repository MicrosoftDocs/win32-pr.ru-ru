---
description: Метод Листкардинтерфацес извлекает идентификаторы (GUID) всех интерфейсов, поддерживаемых для указанной смарт-карты.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Метод Искарддатабасе:: Листкардинтерфацес (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b97569f967c76c985eb05099a21ed10e90456563a871f3e5d9803c6a5875ebdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008112"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a>Метод Искарддатабасе:: Листкардинтерфацес

\[Метод **листкардинтерфацес** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **листкардинтерфацес** извлекает идентификаторы (GUID) всех интерфейсов, поддерживаемых для указанной [*смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстркарднаме* \[ окне\]
</dt> <dd>

Имя смарт-карты.

</dd> <dt>

*ппинтерфацегуидс* \[ заполняет\]
</dt> <dd>

Указатель на идентификаторы GUID интерфейса в случае успеха; **Null** , если операция завершилась ошибкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                              |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппинтерфацегуидс* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                                  |



 

## <a name="remarks"></a>Remarks

Чтобы получить [*первичный поставщик услуг*](../secgloss/p-gly.md) смарт-карты, вызовите [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md).

Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md), [*читатели*](../secgloss/r-gly.md)и [*группы читателей*](../secgloss/r-gly.md) , вызовите [**листкардс**](iscarddatabase-listcards.md), [**листреадерс**](iscarddatabase-listreaders.md)и [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано получение идентификаторов интерфейсов, поддерживаемых для указанной смарт-карты.


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скардмгр. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардмгр. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искарддатабасе определен как 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетпровидеркардид**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**искарддатабасе**](iscarddatabase.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**листреадерграупс**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**листреадерс**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
