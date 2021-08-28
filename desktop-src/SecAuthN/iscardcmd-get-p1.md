---
description: Извлекает байт первого параметра (P1) из блока данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: a6648e70-96d8-4b7d-ae6d-8832e38d1c71
title: 'Метод Искардкмд:: get_P1 (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_P1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 94fd7dbe7629ebc3137a6323515d401688dc489cf08c7bb3e6d4262527d4d0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014964"
---
# <a name="iscardcmdget_p1-method"></a>Метод Искардкмд:: Get \_ P1

\[Метод **Get \_ P1** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Get \_ P1** извлекает байт первого параметра (P1) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_P1(
  [out] BYTE *pbyP1
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pbyP1* \[ заполняет\]
</dt> <dd>

Указатель на байт P1 в КАТЕГОРИЯХ APDU при возврате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *pbyP1* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *pbyP1* был передан неверный указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                       |



 

## <a name="remarks"></a>Remarks

Чтобы присвоить параметру P1 новое значение, вызовите метод Set [**\_ P1**](iscardcmd-put-p1.md).

Чтобы получить параметры P2 или P3, вызовите [**Get \_ P2**](iscardcmd-get-p2.md) и [**Get \_ P3**](iscardcmd-get-p3.md) соответственно.

Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**искардкмд**](iscardcmd.md).

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как получить байт первого параметра (P1) из [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU). В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
BYTE  byP1;
HRESULT  hr;

// Retrieve the P1 byte.
hr = pISCardCmd->get_P1(&byP1);
if (FAILED(hr))
{
  printf("Failed get_P1\n");
  // Take other error handling action as needed.
}
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

[**получить \_ P2**](iscardcmd-get-p2.md)
</dt> <dt>

[**получение \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> <dt>

[**разместить \_ P1**](iscardcmd-put-p1.md)
</dt> </dl>

 

 
