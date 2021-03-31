---
description: Определяемая приложением функция, которая создает список идентификаторов безопасности (SID), которые применяются к клиенту. Аусзкомпутеграупскаллбакк — это заполнитель для имени определяемой приложением функции.
ms.assetid: c20a02a0-5303-4433-a484-5a89999b32b9
title: Функция обратного вызова Аусзкомпутеграупскаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzComputeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 3728f8114d87d07ddb33dd77a6fda5db30d07cf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819464"
---
# <a name="authzcomputegroupscallback-callback-function"></a>Функция обратного вызова Аусзкомпутеграупскаллбакк

Функция **аусзкомпутеграупскаллбакк** — это определяемая приложением функция, которая создает список [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) (SID), которые применяются к клиенту. **Аусзкомпутеграупскаллбакк** — это заполнитель для имени определяемой приложением функции.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK AuthzComputeGroupsCallback(
  _In_  AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_  PVOID                       Args,
  _Out_ PSID_AND_ATTRIBUTES         *pSidAttrArray,
  _Out_ PDWORD                      pSidCount,
  _Out_ PSID_AND_ATTRIBUTES         *pRestrictedSidAttrArray,
  _Out_ PDWORD                      pRestrictedSidCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хаусзклиентконтекст* \[ окне\]
</dt> <dd>

Маркер контекста клиента.

</dd> <dt>

*Args* \[ окне\]
</dt> <dd>

Данные, передаваемые в параметре *динамикграупаргс* вызова функции [**аусзинитиализеконтекстфромаусзконтекст**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext), [**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)или [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) .

</dd> <dt>

*псидаттраррай* \[ заполняет\]
</dt> <dd>

Указатель на переменную указателя, которая получает адрес массива структур [**SID \_ и \_ атрибутов**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Эти структуры представляют группы, к которым принадлежит клиент.

</dd> <dt>

*псидкаунт* \[ заполняет\]
</dt> <dd>

Количество структур в *псидаттраррай*.

</dd> <dt>

*престриктедсидаттраррай* \[ заполняет\]
</dt> <dd>

Указатель на переменную указателя, которая получает адрес массива структур [**SID \_ и \_ атрибутов**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) . Эти структуры представляют группы, из которых клиент ограничен.

</dd> <dt>

*престриктедсидкаунт* \[ заполняет\]
</dt> <dd>

Количество структур в *псидрестриктедаттраррай*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция успешно возвращает список идентификаторов безопасности, возвращается значение **true**.

Если функция завершается ошибкой, возвращается значение **false**.

## <a name="remarks"></a>Комментарии

Приложения также могут добавлять идентификаторы безопасности в контекст клиента путем вызова [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).

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

[**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)
</dt> <dt>

[**аусзкачедакцессчекк**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[**аусзинитиализеконтекстфромаусзконтекст**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext)
</dt> <dt>

[**аусзинитиализеконтекстфромсид**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid)
</dt> <dt>

[**аусзинитиализеконтекстфромтокен**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken)
</dt> <dt>

[**аусзинитиализересаурцеманажер**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> <dt>

[**Идентификатор безопасности \_ и \_ атрибуты**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes)
</dt> </dl>

 

