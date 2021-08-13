---
description: Windows Функции установщика, возвращающие данные в предоставленном пользователем расположении, не должны вызываться со значением NULL в качестве значения для указателя.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: передача значений null в функции установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6964716479d7e64cc9aa70d7e49acc8fe78dd3343298826e011f6d72b4df1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627667"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>передача значения null в качестве аргумента функций установщик Windows

Windows Функции установщика, возвращающие данные в предоставленном пользователем расположении, не должны вызываться со значением NULL в качестве значения для указателя. Эти функции возвращают строку или возвращают данные в виде целочисленных указателей, но возвращают непротиворечивые значения при передаче значения NULL в качестве аргумента Output.

Не передавайте значение NULL в качестве значения аргумента Output для любой из следующих функций:

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**мсирекорджетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**мсижетсаурцепас**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**мсижеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**мсивиевжетеррор**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**мсисуммаринфожетпроперти**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**мсиевалуатекондитион**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**мсижетфеатурекост**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**мсижетфеатурекост**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**мсижетфеатуревалидстатес**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



