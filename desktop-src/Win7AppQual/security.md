---
description: безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d392f5bf14997962173b9054baba861003877d851d6bd62a947b15757feec23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994664"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)

начиная с Windows internet explorer 7 Windows internet explorer работает в контексте безопасности, который называется *защищенным режимом* , когда пользователи запускают его в операционной системе Windows Vista или более поздней версии. этот режим использует Internet Explorer с более низким уровнем прав, чем стандартное приложение пользователя, поэтому некоторые функциональные возможности ограничены, особенно ActiveX элементы управления и определенные типы подключаемых модулей. дополнительные сведения о защищенном режиме в internet explorer и его влиянии на совместимость см. в разделе [основные сведения и работа в защищенном режиме internet explorer](/previous-versions/windows/internet-explorer/ie-developer/) в библиотека MSDN.

по умолчанию Windows Internet Explorer 8 также включает предотвращение выполнения данных (DEP), что помогает приложениям избегать выполнения произвольного кода в сетевых атаках. однако некоторые надстройки могут не использовать эту функцию безопасности (например, любые надстройки, которые не предназначены для запуска всего кода, который был специально помечен как исполняемый, например приложений, созданных с помощью более старой версии платформы ActiveX шаблонов (ATL)).

Internet Explorer 8 также защищает пользователей от потенциальных уязвимостей системы безопасности, использующих сценарии. Например, нельзя переходить от URL-адреса в зоне с меньшим доверием на URL-адрес в более надежной зоне, за исключением явного взаимодействия с пользователем. Вы также не можете скрыть определенные элементы пользовательского интерфейса браузера (например, адресную строку) в зоне без доверия (Интернет).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разработка обновлений, влияющих на совместимость браузеров](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
