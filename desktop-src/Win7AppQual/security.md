---
description: Безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116232"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)

Начиная с Windows Internet Explorer 7, Windows Internet Explorer работает в контексте безопасности, который называется *защищенным режимом* , когда пользователи работают в операционной системе Windows Vista или более поздней версии. Этот режим использует Internet Explorer с более низким уровнем прав, чем стандартное приложение пользователя, поэтому некоторые функциональные возможности ограничены, особенно элементы управления ActiveX и определенные типы подключаемых модулей. Дополнительные сведения о защищенном режиме в Internet Explorer и его влиянии на совместимость см. в разделе [Основные сведения и работа в защищенном режиме Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) в библиотеке MSDN.

По умолчанию Windows Internet Explorer 8 также включает предотвращение выполнения данных (DEP), что помогает приложениям избегать выполнения произвольного кода в сетевых атаках. Однако некоторые надстройки могут не использовать эту функцию безопасности (например, любые надстройки, которые не предназначены для запуска всего кода, который был специально помечен как исполняемый, например приложений, созданных с помощью более старой версии платформы библиотеки шаблонов ActiveX (ATL)).

Internet Explorer 8 также защищает пользователей от потенциальных уязвимостей системы безопасности, использующих сценарии. Например, нельзя переходить от URL-адреса в зоне с меньшим доверием на URL-адрес в более надежной зоне, за исключением явного взаимодействия с пользователем. Вы также не можете скрыть определенные элементы пользовательского интерфейса браузера (например, адресную строку) в зоне без доверия (Интернет).

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Разработка обновлений, влияющих на совместимость браузеров](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
