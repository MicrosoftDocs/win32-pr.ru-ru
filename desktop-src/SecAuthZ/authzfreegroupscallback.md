---
description: Определяемая приложением функция, которая освобождает память, выделенную функцией Аусзкомпутеграупскаллбакк. Аусзфриграупскаллбакк — это заполнитель для имени определяемой приложением функции.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Функция обратного вызова Аусзфриграупскаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3cce78e261892fede79fb8fc76bc5b0d009342db3e0bf672be2854cb8492bcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783768"
---
# <a name="authzfreegroupscallback-callback-function"></a>Функция обратного вызова Аусзфриграупскаллбакк

Функция **аусзфриграупскаллбакк** является определяемой приложением функцией, которая освобождает память, выделенную функцией [**аусзкомпутеграупскаллбакк**](authzcomputegroupscallback.md) . **Аусзфриграупскаллбакк** — это заполнитель для имени определяемой приложением функции.

## <a name="syntax"></a>Синтаксис


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псидаттраррай* \[ окне\]
</dt> <dd>

Указатель на память, выделенную [**аусзкомпутеграупскаллбакк**](authzcomputegroupscallback.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция обратного вызова не возвращает значение.

## <a name="remarks"></a>Remarks

Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                   |
| Распространяемые компоненты<br/>          | Windows пакет средств администрирования сервера 2003 в Windows XP<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основные функции контроля доступа](authorization-functions.md)
</dt> <dt>

[**аусзкомпутеграупскаллбакк**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




