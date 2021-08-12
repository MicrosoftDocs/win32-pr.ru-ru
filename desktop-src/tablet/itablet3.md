---
description: Интерфейс ITablet3 позволяет Мультисенсорная запросы входных данных.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Интерфейс ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449847"
---
# <a name="itablet3-interface"></a>Интерфейс ITablet3

Интерфейс ITablet3 позволяет Мультисенсорная запросы входных данных.

## <a name="members"></a>Элементы

Интерфейс **ITablet3** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet3** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ITablet3** содержит следующие методы.



| Метод                                                  | Описание                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**жетмаксимумкурсорс**](itablet3-getmaximumcursors.md) | Возвращает максимальное число поддерживаемых входных данных.<br/>        |
| [**исмултитауч**](itablet3-ismultitouch.md)           | Указывает, включен ли Мультисенсорная для этого объекта.<br/> |



 

## <a name="remarks"></a>Remarks

Разработчики не должны использовать этот интерфейс

В следующем коде показано, как определяется интерфейс **ITablet3** .

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

