---
description: Метод Листреадерс извлекает имена устройств чтения смарт-карт, зарегистрированных в базе данных смарт-карты.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'Метод Искарддатабасе:: Листреадерс (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c7ae9c41a8b1894ec0c233c6090f8ab990e275e95bc20c4768171fe867412838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141137"
---
# <a name="iscarddatabaselistreaders-method"></a>Метод Искарддатабасе:: Листреадерс

\[Метод **листреадерс** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **листреадерс** извлекает имена [*устройств чтения*](../secgloss/r-gly.md) смарт-карт, зарегистрированных в [*базе данных смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*LocaleID* \[ окне\]
</dt> <dd>

ИДЕНТИФИКАТОР локализации языка.

</dd> <dt>

*ппреадерс* \[ заполняет\]
</dt> <dd>

Указатель на массив SAFEARRAY элементов BSTR, содержащий имена устройств чтения смарт-карт в случае успеха; **Значение NULL** , если операция завершилась ошибкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                       |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппреадерс* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                           |



 

## <a name="remarks"></a>Remarks

Чтобы получить все известные [*смарт-карты*](../secgloss/s-gly.md) или [*группы читателей*](../secgloss/r-gly.md), вызовите [**листкардс**](iscarddatabase-listcards.md) или [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.

Получение [*первичного поставщика услуг*](../secgloss/p-gly.md) или интерфейсов конкретного адаптера [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md) или [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано получение имен устройств чтения смарт-карт, зарегистрированных в базе данных смарт-карты.


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
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

[**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**листреадерграупс**](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
