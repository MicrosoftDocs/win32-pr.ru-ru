---
title: Определение интерфейса
description: Определение интерфейса — это формальное описание того, как клиентское приложение и серверное приложение взаимодействуют друг с другом.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Удаленный вызов процедур RPC, задачи, определение интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067657"
---
# <a name="defining-the-interface"></a><span data-ttu-id="bf4df-104">Определение интерфейса</span><span class="sxs-lookup"><span data-stu-id="bf4df-104">Defining the Interface</span></span>

<span data-ttu-id="bf4df-105">Определение интерфейса — это формальное описание того, как клиентское приложение и серверное приложение взаимодействуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bf4df-105">An interface definition is a formal specification for how a client application and a server application communicate with each other.</span></span> <span data-ttu-id="bf4df-106">Интерфейс определяет, как клиент и сервер распознают друг друга, удаленные процедуры, которые может вызывать клиентское приложение, и типы данных для параметров и возвращаемых значений процедур.</span><span class="sxs-lookup"><span data-stu-id="bf4df-106">The interface defines how the client and server recognize each other, the remote procedures that the client application can call, and the data types for those procedures' parameters and return values.</span></span> <span data-ttu-id="bf4df-107">Он также указывает, как передаются данные между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="bf4df-107">It also specifies how the data is transmitted between client and server.</span></span>

<span data-ttu-id="bf4df-108">Этот интерфейс определяется в язык MIDL (MIDL), который состоит из определений языка C, дополненных ключевыми словами, которые называются атрибутами, описывающими передачу данных по сети.</span><span class="sxs-lookup"><span data-stu-id="bf4df-108">You define this interface in the Microsoft Interface Definition Language (MIDL) which consists of C-language definitions augmented with keywords, called attributes, which describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="bf4df-109">В файле определения интерфейса (IDL) содержатся определения типов, атрибуты и прототипы функций, описывающие передачу данных в сети.</span><span class="sxs-lookup"><span data-stu-id="bf4df-109">The interface definition (IDL) file contains type definitions, attributes and function prototypes that describe how data is transmitted on the network.</span></span> <span data-ttu-id="bf4df-110">Файл конфигурации приложения (ACF) содержит атрибуты, которые настраивают приложение для конкретной операционной среды, не влияя на характеристики сети.</span><span class="sxs-lookup"><span data-stu-id="bf4df-110">The application configuration (ACF) file contains attributes that configure your application for a particular operating environment without affecting its network characteristics.</span></span>

 

 




