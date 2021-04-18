---
description: Метод Селектпаренталлевел задает указанный родительский уровень для последующего воспроизведения.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Метод Селектпаренталлевел
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537106"
---
# <a name="selectparentallevel-method"></a>Метод Селектпаренталлевел

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

## <a name="remarks"></a>Комментарии

Этот метод задает уровень доступа в объекте Мсвебдвд, который определяет, какое содержимое может воспроизводить пользователь. Более высокие уровни могут воспроизводить содержимое нижнего уровня, но более низкие уровни не могут воспроизвести содержимое более высокого уровня. Точное значение восьми уровней родительского управления DVD зависит от страны или региона. В США и Канаде уровни сопоставлены с категориями рейтинга «Ассоциация движения» для «America» (МПАА). По умолчанию функция родительского управления в навигаторе DVD отключена.

## <a name="see-also"></a>См. также раздел

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

 

 



