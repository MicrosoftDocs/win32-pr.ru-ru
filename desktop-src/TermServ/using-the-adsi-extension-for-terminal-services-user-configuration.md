---
title: Использование расширения ADSI для службы удаленных рабочих столов пользовательской конфигурации
description: Администрирование пользовательских свойств, связанных с службы удаленных рабочих столов, возможно с помощью методов, реализованных расширением интерфейсов служб Active Directory (ADSI), упакованных с помощью Tsuserex.dll библиотеки динамической компоновки.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов службы удаленных рабочих столов с помощью расширения ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987815"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="8f937-104">Использование расширения ADSI для службы удаленных рабочих столов пользовательской конфигурации</span><span class="sxs-lookup"><span data-stu-id="8f937-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="8f937-105">Расширение "интерфейсы служб Active Directory (ADSI) для службы удаленных рабочих столов пользовательской конфигурации — это библиотека, упакованная с помощью Tsuserex.dll библиотеки динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="8f937-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="8f937-106">Администрирование пользовательских свойств, связанных с службы удаленных рабочих столов, возможно с помощью методов, реализованных в расширении.</span><span class="sxs-lookup"><span data-stu-id="8f937-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="8f937-107">Методы позволяют настраивать свойства, доступные в интерфейсе расширения для пользователей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8f937-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="8f937-108">Расширение ADSI для службы удаленных рабочих столов пользовательской конфигурации поддерживает изучение и обработку службы удаленных рабочих столов пользовательских свойств, хранящихся в базе данных службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="8f937-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="8f937-109">Расширение также поддерживает настройку свойств пользователей, которые хранятся в Active Directory с помощью API протокола LDAP.</span><span class="sxs-lookup"><span data-stu-id="8f937-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="8f937-110">Поставщик реализует следующие методы:</span><span class="sxs-lookup"><span data-stu-id="8f937-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="8f937-111">[**IAds:: Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span><span class="sxs-lookup"><span data-stu-id="8f937-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="8f937-112">Этот метод выполняет поиск конкретного свойства или набора свойств в экземпляре класса.</span><span class="sxs-lookup"><span data-stu-id="8f937-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="8f937-113">[**IAds::P UT**](/windows/desktop/api/iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="8f937-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="8f937-114">Этот метод настраивает определенное свойство или набор свойств в экземпляре класса.</span><span class="sxs-lookup"><span data-stu-id="8f937-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="8f937-115">Список определяемых пользователем свойств службы удаленных рабочих столов, которые можно настроить, см. в [справочнике по расширению ADSI для службы удаленных рабочих столов пользовательской конфигурации](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="8f937-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="8f937-116">Дополнительные сведения о доступе к атрибутам и их изменении с помощью ADSI см. в разделе [доступ к данным и управление ими с помощью ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span><span class="sxs-lookup"><span data-stu-id="8f937-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="8f937-117">Дополнительные сведения об использовании соглашений об именовании ADSI и AdsPath-строк см. в разделе сведения об отдельных [поставщиках служб ADSI](/windows/desktop/ADSI/adsi-system-providers) в документации по службам [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8f937-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 