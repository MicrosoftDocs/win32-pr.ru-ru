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
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712814"
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



 

## <a name="remarks"></a>Комментарии

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

