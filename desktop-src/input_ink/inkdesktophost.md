---
description: Реализует интерфейс Иинкдесктофост.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Класс Инкдесктофост
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105720013"
---
# <a name="inkdesktophost-class"></a>Класс Инкдесктофост

Реализует интерфейс [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .

Объект [**иинкдесктофост**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) обеспечивает рукописный ввод, обработку и отрисовку посредством создания потока приложения для размещения объекта [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) и вставки его в визуальное дерево [DirectComposition](../directcomp/directcomposition-portal.md) приложения.

## <a name="members"></a>Элементы

Класс **инкдесктофост** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Инкдесктофост** также имеет следующие типы членов:

- [Методы](#methods)

### <a name="methods"></a>Методы

Класс **инкдесктофост** содержит следующие методы.

| Метод | Описание |
|---|---|
| [**креатеандинитиализеинкпресентер**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Создает объект [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) в потоке приложения, подключает его к визуальному дереву [DirectComposition](../directcomp/directcomposition-portal.md) приложения и задает размер объекта.<br/> |
| [**креатеинкпресентер**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Создает объект [**иинкпресентердесктоп**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) в потоке приложения.<br/> |
| [**куеуеворкитем**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Добавьте операцию рукописного ввода в рабочую очередь для выполнения в потоке **инкдесктофост** .<br/> |

## <a name="creationaccess-functions"></a>\\Функции доступа для создания

Вызовите [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса <strong>инкдесктофост</strong> , чтобы получить ссылку на объект.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a>Требования

| Требование | Значение |
|---|---|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/> |
| Header<br/>                   | <dl> <dt>Инкпресентердесктоп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Инкпресентердесктоп. idl</dt> </dl> |
| IID<br/>                      | IID \_ иинкдесктофост определен как 4ce7d875-a981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>См. также

[Классы для рукописного ввода](ink-presenter-classes.md), [взаимодействие пером и](/windows/uwp/design/input/pen-and-stylus-interactions)пера, [Пример анализа рукописного ввода](/samples/microsoft/windows-universal-samples/inkanalysis/), [простой пример](/samples/microsoft/windows-universal-samples/simpleink/)с рукописным вводом, [сложный пример для рукописного](/samples/microsoft/windows-universal-samples/complexink/) ввода
