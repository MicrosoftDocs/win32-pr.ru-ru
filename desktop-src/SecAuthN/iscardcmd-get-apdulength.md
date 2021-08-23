---
description: Определяет длину (в байтах) f в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'Метод Искардкмд:: get_ApduLength (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: be2dc0ed209f4d7be5c36be25579c69149c554ab159590339297b4180f461062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577744"
---
# <a name="iscardcmdget_apdulength-method"></a>Метод Искардкмд:: Get \_ апдуленгс

\[Метод **Get \_ апдуленгс** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Get \_ апдуленгс** определяет длину (в байтах) f в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плсизе* \[ заполняет\]
</dt> <dd>

Указатель на длину КАТЕГОРИЯХ APDU.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *плсизе* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *плсизе* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                        |



 

## <a name="remarks"></a>Remarks

Чтобы получить необработанную [*единицу данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU) из буфера байтов, сопоставленного с помощью **IStream** , содержащего сообщение категориях APDU, вызовите [**Get \_ категориях APDU**](iscardcmd-get-apdu.md).

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как получить длину [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU). В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скарддат. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скарддат. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**получить \_ категориях APDU**](iscardcmd-get-apdu.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
