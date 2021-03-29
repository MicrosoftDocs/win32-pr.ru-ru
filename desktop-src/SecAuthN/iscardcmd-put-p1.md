---
description: Задает первый байт параметра (P1) для единицы данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 359df5cc-10a7-4093-9a77-f3eb0b98545a
title: 'Искардкмд: метод ut_P1:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 18f7563fd6ae1c3490e36896b22af3a6034168e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647483"
---
# <a name="iscardcmdput_p1-method"></a>Искардкмд: метод:p UT \_ P1

\[Метод **размещения \_ P1** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **размещения \_ P1** задает первый байт параметра (P1) для [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_P1(
  [in] BYTE byP1
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*byP1* \[ окне\]
</dt> <dd>

Байт, который является полем P1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *byP1* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                     |



 

## <a name="remarks"></a>Комментарии

Чтобы задать значение P2 объекта КАТЕГОРИЯХ APDU, вызовите [**Get \_ P2**](iscardcmd-get-p2.md).

Чтобы получить существующие значения P1, P2 и P3, вызовите [**Get \_ P1**](iscardcmd-get-p1.md), [**Get \_ P2**](iscardcmd-get-p2.md) или [**Get \_ P3**](iscardcmd-get-p3.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как задать байт первого параметра (P1) для [*единицы данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU). В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
HRESULT  hr;

// Set the P1 byte.
hr = pISCardCmd->put_P1(0x06);
if (FAILED(hr))
{
  printf("Failed put_P1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Скарддат. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скарддат. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искардкмд определен как D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**получить \_ P1**](iscardcmd-get-p1.md)
</dt> <dt>

[**получить \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**получение \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> <dt>

[**разместить \_ P2**](iscardcmd-put-p2.md)
</dt> </dl>

 

 
