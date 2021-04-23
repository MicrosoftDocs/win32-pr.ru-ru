---
title: Получение удостоверения кодировки
description: Приложение, которое декодирует закодированные данные, может получить удостоверение подпрограммы, используемой для кодирования данных, до вызова подпрограммы для декодирования. Подпрограммы Месинкпроценкодингид предоставляют это удостоверение.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Удаленный вызов процедур RPC, задачи, получение удостоверения кодировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778608"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="3fc08-105">Получение удостоверения кодировки</span><span class="sxs-lookup"><span data-stu-id="3fc08-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="3fc08-106">Приложение, которое декодирует закодированные данные, может получить удостоверение подпрограммы, используемой для кодирования данных, до вызова подпрограммы для декодирования.</span><span class="sxs-lookup"><span data-stu-id="3fc08-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="3fc08-107">Подпрограммы [**месинкпроценкодингид**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) предоставляют это удостоверение.</span><span class="sxs-lookup"><span data-stu-id="3fc08-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="3fc08-108">Каждой процедуре в интерфейсе присваивается целочисленный идентификационный номер, называемый *идентификатором процедуры* или *идентификатором процесса*, компилятором MIDL.</span><span class="sxs-lookup"><span data-stu-id="3fc08-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="3fc08-109">Нумерация начинается с нуля.</span><span class="sxs-lookup"><span data-stu-id="3fc08-109">Numbering begins with zero.</span></span> <span data-ttu-id="3fc08-110">Библиотеки времени выполнения RPC не участвуют в преобразовании идентификатора процедуры в фактический вызов процедуры.</span><span class="sxs-lookup"><span data-stu-id="3fc08-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="3fc08-111">При наличии идентификатора процесса приложение должно предоставлять средства вызова правильной процедуры.</span><span class="sxs-lookup"><span data-stu-id="3fc08-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="3fc08-112">Как правило, разработчики приложений используют последовательность операторов **If** или (при использовании C/C++) оператор **switch** для этой цели.</span><span class="sxs-lookup"><span data-stu-id="3fc08-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 




