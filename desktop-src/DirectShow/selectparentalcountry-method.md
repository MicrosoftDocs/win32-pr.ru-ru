---
description: Метод Селектпаренталкаунтри задает указанную локальную страну или регион для последующего воспроизведения.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Метод Селектпаренталкаунтри
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537787"
---
# <a name="selectparentalcountry-method"></a>Метод Селектпаренталкаунтри

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

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

## <a name="remarks"></a>Комментарии

Родительский регион определяет, как обрабатываются родительские уровни.

## <a name="see-also"></a>См. также раздел

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

 

 



