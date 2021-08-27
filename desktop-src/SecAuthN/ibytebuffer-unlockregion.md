---
description: 'Удаляет ограничение доступа для диапазона байтов, которые ранее были ограничены с помощью Ибитебуффер:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Метод Ибитебуффер:: UnlockRegion (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 798569621c1a46e73ea6fd8e2f4f3333c3a0cbcef32618797fcba39d35b55bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127394"
---
# <a name="ibytebufferunlockregion-method"></a>Метод Ибитебуффер:: UnlockRegion

\[Метод **UnlockRegion** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]

Метод **UnlockRegion** удаляет ограничение доступа для диапазона байтов, которые ранее были ограничены с помощью [**Ибитебуффер:: LockRegion**](ibytebuffer-lockregion.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*либоффсет* \[ окне\]
</dt> <dd>

Смещение в байтах для начала диапазона.

</dd> <dt>

*CB* \[ окне\]
</dt> <dd>

Длина (в байтах) диапазона, который должен быть ограничен.

</dd> <dt>

*двлокктипе* \[ окне\]
</dt> <dd>

Ограничения доступа, ранее помещенные в диапазон.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает на Успешный вызов.

## <a name="remarks"></a>Remarks

Метод **ибитебуффер:: UnlockRegion** разблокирует область, ранее заблокированную с помощью метода [**Ибитебуффер:: LockRegion**](ibytebuffer-lockregion.md) . Заблокированные регионы позже должны быть явным образом разблокированы путем вызова **ибитебуффер:: UnlockRegion** с теми же значениями параметров *либоффсет*, *CB* и *двлокктипе* . Перед освобождением потока необходимо разблокировать регион. Два смежных региона не могут быть заблокированы отдельно, а затем разблокированы с помощью одного вызова Unlock.

## <a name="examples"></a>Примеры

В следующем примере показано Разблокирование диапазона байтов.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
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



 

