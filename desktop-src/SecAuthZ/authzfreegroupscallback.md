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
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819457"
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

## <a name="remarks"></a>Комментарии

Переменные атрибутов должны быть выражены в виде выражения при использовании с логическими операторами. в противном случае они оцениваются как неизвестные.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |
| Распространяемые компоненты<br/>          | Пакет средств администрирования Windows Server 2003 в Windows XP<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основные функции контроля доступа](authorization-functions.md)
</dt> <dt>

[**аусзкомпутеграупскаллбакк**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




