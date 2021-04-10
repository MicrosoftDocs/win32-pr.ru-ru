---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273090"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="5f555-103">Безопасность (Windows 7 и Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="5f555-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="5f555-104">Начиная с Windows Internet Explorer 7, Windows Internet Explorer работает в контексте безопасности, который называется *защищенным режимом* , когда пользователи работают в операционной системе Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5f555-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="5f555-105">Этот режим использует Internet Explorer с более низким уровнем прав, чем стандартное приложение пользователя, поэтому некоторые функциональные возможности ограничены, особенно элементы управления ActiveX и определенные типы подключаемых модулей. Дополнительные сведения о защищенном режиме в Internet Explorer и его влиянии на совместимость см. в разделе [Основные сведения и работа в защищенном режиме Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) в библиотеке MSDN.</span><span class="sxs-lookup"><span data-stu-id="5f555-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="5f555-106">По умолчанию Windows Internet Explorer 8 также включает предотвращение выполнения данных (DEP), что помогает приложениям избегать выполнения произвольного кода в сетевых атаках.</span><span class="sxs-lookup"><span data-stu-id="5f555-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="5f555-107">Однако некоторые надстройки могут не использовать эту функцию безопасности (например, любые надстройки, которые не предназначены для запуска всего кода, который был специально помечен как исполняемый, например приложений, созданных с помощью более старой версии платформы библиотеки шаблонов ActiveX (ATL)).</span><span class="sxs-lookup"><span data-stu-id="5f555-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="5f555-108">Internet Explorer 8 также защищает пользователей от потенциальных уязвимостей системы безопасности, использующих сценарии.</span><span class="sxs-lookup"><span data-stu-id="5f555-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="5f555-109">Например, нельзя переходить от URL-адреса в зоне с меньшим доверием на URL-адрес в более надежной зоне, за исключением явного взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="5f555-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="5f555-110">Вы также не можете скрыть определенные элементы пользовательского интерфейса браузера (например, адресную строку) в зоне без доверия (Интернет).</span><span class="sxs-lookup"><span data-stu-id="5f555-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f555-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5f555-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f555-112">Разработка обновлений, влияющих на совместимость браузеров</span><span class="sxs-lookup"><span data-stu-id="5f555-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
