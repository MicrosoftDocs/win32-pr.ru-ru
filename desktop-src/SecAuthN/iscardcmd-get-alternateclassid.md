---
description: Возвращает значение идентификатора альтернативного класса.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Метод Искардкмд:: get_AlternateClassId (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647613"
---
# <a name="iscardcmdget_alternateclassid-method"></a>Метод Искардкмд:: Get \_ алтернатеклассид

\[Метод **Get \_ алтернатеклассид** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **Get \_ алтернатеклассид** извлекает значение идентификатора альтернативного класса. Этот метод завершится ошибкой, если альтернативный идентификатор не был задан предыдущим вызовом метода Set [**\_ алтернатеклассид**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбикласс* \[ заполняет\]
</dt> <dd>

Указатель на байт, содержащий альтернативное значение идентификатора класса при возврате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает следующие возможные значения.



| Код возврата                                                                                    | Описание                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>           | Операция успешно завершена.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Недопустимый параметр *пбикласс* .<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Альтернативный идентификатор класса не был ранее задан вызовом метода Set [**\_ алтернатеклассид**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод применяется к обмену данными с помощью [*протокола T = 0*](../secgloss/t-gly.md). Дополнительные сведения см. в разделе [**Размещение \_ алтернатеклассид**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как получить альтернативный идентификатор класса. В примере предполагается, что Пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
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

[**искардкмд**](iscardcmd.md)
</dt> <dt>

[**разместить \_ алтернатеклассид**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
