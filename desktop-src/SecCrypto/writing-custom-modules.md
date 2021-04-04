---
description: Модули политики можно писать на языке программирования C, C++ или Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Написание пользовательских модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998625"
---
# <a name="writing-custom-modules"></a><span data-ttu-id="d8a80-103">Написание пользовательских модулей</span><span class="sxs-lookup"><span data-stu-id="d8a80-103">Writing Custom Modules</span></span>

<span data-ttu-id="d8a80-104">Модули политики можно писать на языке программирования C, C++ или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d8a80-104">You can write policy modules in the C, C++, or Visual Basic programming language.</span></span> <span data-ttu-id="d8a80-105">Необходимый компилятор Microsoft доступен в Visual C++ версии 5,0 или более поздней или в Visual Basic версии 5,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d8a80-105">The required Microsoft compiler is available in Visual C++ version 5.0 or later or in Visual Basic version 5.0 or later.</span></span> <span data-ttu-id="d8a80-106">В [*центре сертификации*](../secgloss/c-gly.md) предприятия (ЦС) должен использоваться только модуль политики предприятия, предоставленный корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d8a80-106">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

<span data-ttu-id="d8a80-107">При написании пользовательского модуля политики необходимо реализовать [**ицертполици**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) .</span><span class="sxs-lookup"><span data-stu-id="d8a80-107">You must implement [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) when writing a custom policy module.</span></span> <span data-ttu-id="d8a80-108">Кроме того, при написании пользовательского модуля политики необходимо реализовать [**ицертманажемодуле**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) .</span><span class="sxs-lookup"><span data-stu-id="d8a80-108">Additionally, you must implement [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) when writing a custom policy module.</span></span>

<span data-ttu-id="d8a80-109">Модули политики могут вызывать методы из [**ицертсерверполици**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) для помощи в обработке [*запроса на сертификат*](../secgloss/c-gly.md); **Ицертсерверполици** позволяет задавать и получать свойства и расширения сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d8a80-109">Policy modules can call methods from [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) to assist in the processing of a [*certificate request*](../secgloss/c-gly.md); **ICertServerPolicy** allows properties and certificate extensions to be set and retrieved.</span></span>

<span data-ttu-id="d8a80-110">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="d8a80-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="d8a80-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="d8a80-111">Topic</span></span>                                                                      | <span data-ttu-id="d8a80-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d8a80-112">Description</span></span>                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="d8a80-113">Настройка свойств сертификата</span><span class="sxs-lookup"><span data-stu-id="d8a80-113">Setting Certificate Properties</span></span>](setting-certificate-properties.md)       | <span data-ttu-id="d8a80-114">Задание свойств сертификата</span><span class="sxs-lookup"><span data-stu-id="d8a80-114">Setting the properties of a certificate</span></span> |
| [<span data-ttu-id="d8a80-115">Написание пользовательских модулей выхода</span><span class="sxs-lookup"><span data-stu-id="d8a80-115">Writing Custom Exit Modules</span></span>](writing-custom-exit-modules.md)             | <span data-ttu-id="d8a80-116">Написание пользовательских модулей выхода</span><span class="sxs-lookup"><span data-stu-id="d8a80-116">Writing custom exit modules</span></span>             |
| [<span data-ttu-id="d8a80-117">Написание пользовательских обработчиков расширений</span><span class="sxs-lookup"><span data-stu-id="d8a80-117">Writing Custom Extension Handlers</span></span>](writing-custom-extension-handlers.md) | <span data-ttu-id="d8a80-118">Написание пользовательских обработчиков расширений</span><span class="sxs-lookup"><span data-stu-id="d8a80-118">Writing custom extension handlers</span></span>       |



 

 

 
