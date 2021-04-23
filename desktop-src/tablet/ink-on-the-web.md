---
description: Пакет средств разработки Windows Vista Software Development Kit и Windows XP Tablet PC Edition позволяют создавать веб-приложения с поддержкой рукописного ввода для пользователей планшетных ПК, которым необходим доступ к удаленным приложениям.
ms.assetid: 4ba1ab4b-57d2-40da-a7c7-2402f8845ff5
title: Рукописный ввод в Интернете
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3584fdc0f19cbf9ac1a60e8f1607971165077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143924"
---
# <a name="ink-on-the-web"></a><span data-ttu-id="00c92-103">Рукописный ввод в Интернете</span><span class="sxs-lookup"><span data-stu-id="00c92-103">Ink on the Web</span></span>

<span data-ttu-id="00c92-104">Пакет средств разработки Windows Vista Software Development Kit и Windows XP Tablet PC Edition позволяют создавать веб-приложения с поддержкой рукописного ввода для пользователей планшетных ПК, которым необходим доступ к удаленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="00c92-104">The Windows Vista Software Development Kit and Windows XP Tablet PC Edition Development Kit allow you to create ink-enabled web applications for Tablet PC users who must access remote applications.</span></span> <span data-ttu-id="00c92-105">Это можно сделать двумя основными методами. это не сенсорный развертывание, которое позволяет развертывать приложения .NET с веб-сервера или с файловым сервером, а другой — создавать веб-страницы с поддержкой рукописного ввода с помощью элементов управления Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="00c92-105">There are two basic techniques for accomplishing this: one is no-touch deployment, which allows .NET applications to be deployed from a Web or file server, and the other is to create ink-enabled Web pages with Windows Forms controls.</span></span> <span data-ttu-id="00c92-106">В обоих случаях рукописный ввод обрабатывается на клиенте, а не на сервере.</span><span class="sxs-lookup"><span data-stu-id="00c92-106">In both cases, the ink is handled on the client, rather than the server.</span></span> <span data-ttu-id="00c92-107">Обратите внимание, что COM API не поддерживается для веб-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="00c92-107">Note that the COM API is not supported for the Web.</span></span>

<span data-ttu-id="00c92-108">Чтобы использовать обработку на стороне клиента в Интернете, необходимо понимать модель безопасности .NET и то, как работа в рамках частичного доверия влияет на приложение.</span><span class="sxs-lookup"><span data-stu-id="00c92-108">To use client-side processing over the Web, you need to understand the .NET security model and how operating under partial trust affects your application.</span></span> <span data-ttu-id="00c92-109">По этой причине также обсуждается безопасность и доверие для приложений планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="00c92-109">For this reason, security and trust for Tablet PC applications is discussed as well.</span></span>

<span data-ttu-id="00c92-110">В следующих разделах содержатся заметки о различных способах создания веб-приложений с поддержкой рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="00c92-110">The following topics contain notes on various ways of creating ink-enabled Web applications.</span></span>

-   [<span data-ttu-id="00c92-111">Без сенсорного развертывания</span><span class="sxs-lookup"><span data-stu-id="00c92-111">No Touch Deployment</span></span>](no-touch-deployment.md)
-   [<span data-ttu-id="00c92-112">Веб-элементы управления</span><span class="sxs-lookup"><span data-stu-id="00c92-112">Web Controls</span></span>](web-controls.md)
-   [<span data-ttu-id="00c92-113">Веб-приложения с поддержкой рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="00c92-113">Ink-Enabled Web Applications</span></span>](ink-enabled-web-applications.md)
-   [<span data-ttu-id="00c92-114">Безопасность и доверие</span><span class="sxs-lookup"><span data-stu-id="00c92-114">Security and Trust</span></span>](security-and-trust.md)

 

 



