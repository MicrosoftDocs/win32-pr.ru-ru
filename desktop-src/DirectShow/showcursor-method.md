---
description: Метод Шовкурсор делает курсор видимым, когда объект Мсвебдвд находится в полноэкранном режиме.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Метод Шовкурсор
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894766"
---
# <a name="showcursor-method"></a>Метод Шовкурсор

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`ShowCursor`Метод делает курсор видимым, когда объект **мсвебдвд** находится в полноэкранном режиме.

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*бшов*
</dt> <dd>

Указывает, следует ли отображать курсор в виде логического значения.



| Значение | Описание            |
|-------|------------------------|
| true  | Отображение курсора        |
| false | Не показывать курсор |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Когда дисплей DVD переходит в полноэкранный режим, курсор исчезает в течение 3 – 5 секунд. Используйте этот метод, чтобы сделать курсор снова видимым, если кнопки управления приложения видимы в полноэкранном режиме.

 

 



