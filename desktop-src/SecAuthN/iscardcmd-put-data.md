---
description: Задает поле данных в блоке данных протокола приложения (КАТЕГОРИЯХ APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'Искардкмд: метод ut_Data:p (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155106"
---
# <a name="iscardcmdput_data-method"></a>Искардкмд::p \_ метод данных UT

\[Метод **размещения \_ данных** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **размещения \_ данных** задает поле данных в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Указатель на объект буфера байтов (**IStream**), который должен быть скопирован в поле данных категориях APDU.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений.



| Код возврата                                                                                   | Описание                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Operation completed successfully (Операция выполнена успешно).<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *pData* .<br/>  |
| <dl> <dt>**\_указатель E**</dt> </dl>     | В *pData* передан недопустимый указатель.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти.<br/>                       |



 

## <a name="remarks"></a>Комментарии

При установке новой части данных сообщения длина поля данных вычисляется и сохраняется в параметре P3 объекта КАТЕГОРИЯХ APDU. Чтобы получить длину поля данных, вызовите [**Get \_ P3**](iscardcmd-get-p3.md).

Чтобы получить поле данных из КАТЕГОРИЯХ APDU, вызовите [**Get \_ Data**](iscardcmd-get-data.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как задать поле данных в [*блоке данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU). В примере предполагается, что Пибитедата является допустимым указателем на экземпляр интерфейса [**ибитебуффер**](ibytebuffer.md) , а пискардкмд является допустимым указателем на экземпляр интерфейса [**искардкмд**](iscardcmd.md) .


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
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

[**получение \_ данных**](iscardcmd-get-data.md)
</dt> <dt>

[**получение \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**искардкмд**](iscardcmd.md)
</dt> </dl>

 

 
