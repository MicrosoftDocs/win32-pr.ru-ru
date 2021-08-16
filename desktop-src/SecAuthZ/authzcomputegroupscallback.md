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
ms.openlocfilehash: 7c30194e4131cbd375192723e23308e1ad5ead69d849ab73857f72ef1d4b0790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784082"
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

## <a name="remarks"></a>Remarks

Приложения также могут добавлять идентификаторы безопасности в контекст клиента путем вызова [**аусзаддсидстоконтекст**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext).

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

 

