---
description: Метод Аттачбиреадер открывает смарт-карту в именованном модуле чтения.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: Метод Аттачбиреадер (Скардмгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999300"
---
# <a name="iscardattachbyreader-method"></a>Метод Аттачбиреадер::

\[Метод **аттачбиреадер** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **аттачбиреадер** открывает [*смарт-карту*](../secgloss/s-gly.md) в именованном [*модуле чтения*](../secgloss/r-gly.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрреадернаме* \[ окне\]
</dt> <dd>

Значение типа **BSTR** , содержащее имя устройства чтения смарт-карт.

</dd> <dt>

*Шаремоде* \[ окне\]
</dt> <dd>

Режим, в котором запрашивать доступ к смарт-карте.



| Значение                                                                                                                                            | Значение                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ВЗАИМОИСКЛЮЧАЮЩИМ**</dt> </dl> | Никто больше не использует это подключение к смарт-карте.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**ИСПОЛЬЗУЕМЫЙ**</dt> </dl>          | Это подключение могут использовать другие приложения.<br/>        |



 

</dd> <dt>

*Префпротокол* \[ окне\]
</dt> <dd>

Предпочтительное значение протокола.

<dl><span id="T0"></span><span id="t0"></span><dt>

**T0**
</dt><span id="T1"></span><span id="t1"></span><dt>

**T1**
</dt><span id="RAW"></span><span id="raw"></span><dt>

**RAW**
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

**T0 \| T1**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                  | Описание                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Открытие на смарт-карте в именованном модуле чтения успешно завершено.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.<br/> |



 

## <a name="remarks"></a>Комментарии

Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты. Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).

После завершения использования модуля чтения отпустите вложение, вызвав метод [**етач::D**](iscard-detach.md) .

## <a name="examples"></a>Примеры

В следующем примере показано подключение к смарт-карте в указанном модуле чтения смарт-карт.


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
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
| IID<br/>                      | Идентификатор IID \_ -карты определен как 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**аттачбихандле**](iscard-attachbyhandle.md)
</dt> <dt>

[**Соединил**](iscard-detach.md)
</dt> <dt>

[**Карточка**](iscard.md)
</dt> <dt>

[**Повторно подключиться**](iscard-reattach.md)
</dt> </dl>

 

 
