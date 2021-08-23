---
description: Метод Селектпаренталкаунтри задает указанную локальную страну или регион для последующего воспроизведения.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Метод Селектпаренталкаунтри
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d148145f2c38cdb01da209e02f6400301da851e1d2b41e5adaf84b2338ad21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684064"
---
# <a name="selectparentalcountry-method"></a>Метод Селектпаренталкаунтри

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SelectParentalCountry`Метод задает указанную родительским страну или регион для последующего воспроизведения.

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*икаунтри*
</dt> <dd>

Указывает страну или регион в виде целого числа.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*сусернаме*
</dt> <dd>

Указывает текущего пользователя, выполнившего вход в систему, в виде строки. (В настоящий момент игнорируется.)

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*спассворд*
</dt> <dd>

Указывает строку пароля приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Remarks

Родительский регион определяет, как обрабатываются родительские уровни.

## <a name="see-also"></a>См. также

<dl> <dt>

[**селектпаренталлевел**](selectparentallevel-method.md)
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

 

 



