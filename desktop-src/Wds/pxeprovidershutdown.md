---
title: Функция обратного вызова Пксепровидершутдовн
description: Вызывается для завершения работы поставщика.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Функция обратного вызова Пксепровидершутдовн службы развертывания Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701045"
---
# <a name="pxeprovidershutdown-callback-function"></a>Функция обратного вызова Пксепровидершутдовн

Вызывается для завершения работы поставщика. Эта функция регистрируется путем вызова функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) с параметром *каллбакктипе* , для которого задано **\_ \_ Отключение обратного вызова PXE**. После вызова этой функции обработчик *хпровидер* , переданный функции [*пксепровидеринитиализе*](pxeproviderinitialize.md) , больше не является допустимым.

## <a name="syntax"></a>Синтаксис


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконтекст* \[ окне\]
</dt> <dd>

Значение контекста, передаваемое функции [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если завершение работы поставщика завершается успешно, обратный вызов должен возвращать **ошибку \_ успешно**. В случае сбоя должен возвращаться соответствующий код ошибки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008, Windows Server 2003 с пакетом обновления 2 (SP2), \[ только классические приложения\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сервера служб развертывания Windows](windows-deployment-services-server-functions.md)
</dt> <dt>

[*пксепровидеринитиализе*](pxeproviderinitialize.md)
</dt> <dt>

[**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





