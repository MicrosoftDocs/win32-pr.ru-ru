---
description: Извлекает строку ATR смарт-карты.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: Метод get_Atr. h.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651096"
---
# <a name="iscardget_atr-method"></a>Метод "кредитной:: Get \_ ATR"

\[Метод **Get \_ ATR** доступен для использования в операционных системах, указанных в разделе требования. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Get \_ ATR** извлекает [*строку ATR*](../secgloss/a-gly.md) [*смарт-карты*](../secgloss/s-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппатр* \[ заполняет\]
</dt> <dd>

Указатель на байтовый буфер в форме [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , который будет содержать строку ATR при возврате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *ппатр* .<br/>           |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *ппатр* был передан неверный указатель.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Память для удовлетворения запроса недоступна.<br/> |



 

## <a name="remarks"></a>Комментарии

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано извлечение строки ATR из смарт-карты.


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
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
| IID<br/>                      | Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**получить \_ кардхандле**](iscard-get-cardhandle.md)
</dt> <dt>

[**получить \_ контекст**](iscard-get-context.md)
</dt> <dt>

[**получить \_ протокол**](iscard-get-protocol.md)
</dt> <dt>

[**получение \_ состояния**](iscard-get-status.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> <dt>

[**Ибитебуффер:: Read**](ibytebuffer-read.md)
</dt> </dl>

 

 
