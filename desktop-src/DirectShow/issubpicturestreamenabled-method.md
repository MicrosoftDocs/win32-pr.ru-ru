---
description: Метод Иссубпиктурестреаменаблед извлекает значение, указывающее, включен ли указанный поток субтитров в текущем заголовке.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Метод Иссубпиктурестреаменаблед
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc982120b6a7a57d59d5213fc57b5ba3851d7d9d2f4c3e553fba97d3307d8bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817051"
---
# <a name="issubpicturestreamenabled-method"></a>Метод Иссубпиктурестреаменаблед

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`IsSubpictureStreamEnabled`Метод получает значение, указывающее, включен ли указанный поток субтитров в текущем заголовке.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Указывает поток субтитров в виде целого числа.



| Значение   | Описание              |
|---------|--------------------------|
| от 0 до 31 | поток субтитров        |
| 63      | выключение потока с низкой скоростью |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает логическое значение, указывающее, доступен ли указанный звуковой поток в текущем заголовке. Значение true означает, что он доступен.

## <a name="remarks"></a>Remarks

Хотя диск может содержать до 32 потоков подизображений, каждый поток необязательно доступен для каждого заголовка. Перед установкой свойства [**куррентсубпиктурестреам**](currentsubpicturestream-property.md) всегда проверяйте, что поток доступен для заголовка.

 

 



