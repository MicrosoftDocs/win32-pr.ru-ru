---
description: Метод Листкардс извлекает все имена смарт-карт, соответствующие указанным идентификаторам интерфейса (GUID), указанную строку ATR или и то, и другое.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Метод Искарддатабасе:: Листкардс (Скардмгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809911"
---
# <a name="iscarddatabaselistcards-method"></a>Метод Искарддатабасе:: Листкардс

\[Метод **листкардс** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **листкардс** извлекает все имена смарт-карт, соответствующие указанным идентификаторам интерфейса (GUID), указанную [*строку ATR*](../secgloss/a-gly.md)или и то, и другое.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Патр* \[ окне\]
</dt> <dd>

Указатель на строку ATR [*смарт-карты*](../secgloss/s-gly.md) . Строка ATR должна быть упакована в [**ибитебуффер**](ibytebuffer.md).

</dd> <dt>

*пинтерфацегуидс* \[ окне\]
</dt> <dd>

Указатель на массив SAFEARRAY идентификаторов COM-интерфейса (GUID) в формате BSTR.

</dd> <dt>

*LocaleID* \[ окне\]
</dt> <dd>

Идентификатор локализации языка.

</dd> <dt>

*ппкарднамес* \[ заполняет\]
</dt> <dd>

Указатель на SAFEARRAY массива типа BSTR, который содержит имена смарт-карт, удовлетворяющих параметрам поиска, если они выполнены успешно. **Значение NULL** , если операция завершилась ошибкой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр.<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Передан неверный указатель.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                    |



 

## <a name="remarks"></a>Комментарии

Чтобы получить все известные [*средства чтения*](../secgloss/r-gly.md) или [*чтения*](../secgloss/r-gly.md), вызовите [**листреадерс**](iscarddatabase-listreaders.md) или [**листреадерграупс**](iscarddatabase-listreadergroups.md) соответственно.

Для получения [*основной службы*](../secgloss/p-gly.md) или интерфейсов определенной карты [**жетпровидеркардид**](iscarddatabase-getprovidercardid.md) или [**листкардинтерфацес**](iscarddatabase-listcardinterfaces.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искарддатабасе**](iscarddatabase.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано получение имен смарт-карт, соответствующих указанной строке ATR.


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
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

[**листреадерграупс**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**листреадерс**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
