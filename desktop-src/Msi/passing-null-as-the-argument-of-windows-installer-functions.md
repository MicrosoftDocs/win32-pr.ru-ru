---
description: Функции установщик Windows, которые возвращают данные в предоставленном пользователем виде, не должны вызываться со значением NULL в качестве значения для указателя.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Передача значений NULL в функции установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650637"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Передача значения NULL в качестве аргумента функций установщик Windows

Функции установщик Windows, которые возвращают данные в предоставленном пользователем виде, не должны вызываться со значением NULL в качестве значения для указателя. Эти функции возвращают строку или возвращают данные в виде целочисленных указателей, но возвращают непротиворечивые значения при передаче значения NULL в качестве аргумента Output.

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

 

 



