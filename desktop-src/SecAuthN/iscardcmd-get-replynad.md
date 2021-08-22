---
description: Извлекает адрес узла (NAD), используемый смарт-картой в ответном сообщении.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Метод Искардкмд:: get_ReplyNad (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 22460acc80aae359b3d31a7e4bf592514dd5c559feb68117d7547a0cdbedf144
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577544"
---
# <a name="iscardcmdget_replynad-method"></a>Метод Искардкмд:: Get \_ реплинад

\[Метод **Get \_ реплинад** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Get \_ реплинад** извлекает адрес узла (NAD), используемый [*смарт-картой*](../secgloss/s-gly.md) в ответном сообщении.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбнад* \[ заполняет\]
</dt> <dd>

Указатель на байт, содержащий NAD, используемый ответным сообщением, при возврате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                    | Описание                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>           | Операция успешно завершена.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Недопустимый параметр *пбнад* .<br/>                     |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Внутренним вызовам не удалось получить сведения об NAD.<br/> |



 

## <a name="remarks"></a>Remarks

Кроме приведенных выше кодов ошибок COM, этот метод может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как получить адрес узла (NAD), используемый [*смарт-картой*](../secgloss/s-gly.md) в ответном сообщении. В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
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

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
