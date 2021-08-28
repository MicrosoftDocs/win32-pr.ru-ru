---
description: Метод stat Получает статистические данные из объекта потока.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Метод Ибитебуффер:: stat (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dd80b408765985b2e009b2e580eb1bf81b08cb5ea1f2e7aaa5ed628a76073a27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127404"
---
# <a name="ibytebufferstat-method"></a>Метод Ибитебуффер:: stat

\[Метод **stat** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]

Метод **stat** получает статистические данные из объекта потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстатстг* \[ заполняет\]
</dt> <dd>

Указывает на структуру **статструкт** , в которой этот метод помещает сведения об этом объекте потока. При возникновении ошибки этот указатель имеет **значение NULL** .

</dd> <dt>

*грфстатфлаг* \[ окне\]
</dt> <dd>

Указывает, что этот метод не возвращает некоторые поля в структуре **статструкт** , тем самым сохраняя операцию выделения памяти. Значения берутся из перечисления [**статфлаг**](/windows/win32/api/wtypes/ne-wtypes-statflag)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает на Успешный вызов.

## <a name="remarks"></a>Remarks

Метод **ибитебуффер:: stat** получает указатель на структуру **статструкт** , содержащую сведения об этом открытом потоке.

## <a name="examples"></a>Примеры

В следующем примере показано получение статистических данных из потока.


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скардссп. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардссп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

