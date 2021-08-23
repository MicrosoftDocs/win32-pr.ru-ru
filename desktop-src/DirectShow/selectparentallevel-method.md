---
description: Метод Селектпаренталлевел задает указанный родительский уровень для последующего воспроизведения.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Метод Селектпаренталлевел
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95de7e8cbf1fb6fa284eddefa1ba07ebb9268825116fdac9c97fbd5d42bac84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684044"
---
# <a name="selectparentallevel-method"></a>Метод Селектпаренталлевел

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SelectParentalLevel`Метод задает указанный родительский уровень для последующего воспроизведения.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*илевел*
</dt> <dd>

Указывает уровень родительского управления в виде целого числа. Чтобы включить функцию родительского управления, параметр *илевел* должен находиться в диапазоне от 1 до 8. Чтобы отключить функцию родительского управления, установите *илевел* в значение-1.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*
</dt> <dd>

Указывает текущего пользователя в виде строки. (В настоящий момент игнорируется.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*
</dt> <dd>

Указывает пароль, который в настоящее время хранится в реестре в виде строки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Этот метод задает уровень доступа в объекте Мсвебдвд, который определяет, какое содержимое может воспроизводить пользователь. Более высокие уровни могут воспроизводить содержимое нижнего уровня, но более низкие уровни не могут воспроизвести содержимое более высокого уровня. Точное значение восьми уровней родительского управления DVD зависит от страны или региона. В США и Канаде уровни сопоставлены с категориями рейтинга «Ассоциация движения» для «America» (МПАА). По умолчанию функция родительского управления в навигаторе DVD отключена.

## <a name="see-also"></a>См. также

<dl> <dt>

[**селектпаренталкаунтри**](selectparentalcountry-method.md)
</dt> <dt>

[**нотифипаренталлевелчанже**](notifyparentallevelchange-method.md)
</dt> <dt>

[**жеттитлепаренталлевелс**](gettitleparentallevels-method.md)
</dt> <dt>

[**жетплайерпаренталкаунтри**](getplayerparentalcountry-method.md)
</dt> <dt>

[**жетплайерпаренталлевел**](getplayerparentallevel-method.md)
</dt> <dt>

[**акцептпаренталлевелчанже**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



