---
description: Сертификаты могут запрашиваться и распространяться с помощью любого транспортного механизма.
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: Независимость от транспорта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8d68b8f6312495c242f6b2bd2ea75301f802c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647211"
---
# <a name="transport-independence"></a><span data-ttu-id="0d34a-103">Независимость от транспорта</span><span class="sxs-lookup"><span data-stu-id="0d34a-103">Transport Independence</span></span>

<span data-ttu-id="0d34a-104">Сертификаты могут запрашиваться и распространяться с помощью любого транспортного механизма.</span><span class="sxs-lookup"><span data-stu-id="0d34a-104">Certificates can be requested and distributed through any transport mechanism.</span></span> <span data-ttu-id="0d34a-105">Службы сертификатов принимают [*запросы на сертификаты*](../secgloss/c-gly.md) от кандидата по протоколу HTTP, DCOM, RPC, Disk File или пользовательским транспортом.</span><span class="sxs-lookup"><span data-stu-id="0d34a-105">Certificate Services accepts [*certificate requests*](../secgloss/c-gly.md) from an applicant through HTTP, DCOM, RPC, disk file, or by custom transport.</span></span> <span data-ttu-id="0d34a-106">Службы сертификатов относят сертификаты кандидату по протоколу HTTP, DCOM, RPC, дискового файла или пользовательскому транспорту.</span><span class="sxs-lookup"><span data-stu-id="0d34a-106">Certificate Services posts certificates to the applicant through HTTP, DCOM, RPC, disk file, or custom transport.</span></span>

<span data-ttu-id="0d34a-107">Транспорты поддерживаются промежуточными приложениями и выходными библиотеками DLL модуля, обычно написанными на C/C++.</span><span class="sxs-lookup"><span data-stu-id="0d34a-107">Transports are supported by intermediary applications and exit module DLLs, usually written in C/C++.</span></span> <span data-ttu-id="0d34a-108">Промежуточные приложения и модули выхода изолируют функции служб сертификации от взаимодействия с любым конкретным транспортом.</span><span class="sxs-lookup"><span data-stu-id="0d34a-108">The intermediary applications and exit modules isolate Certificate Services functions from communicating with any specific transport.</span></span>

 

 
