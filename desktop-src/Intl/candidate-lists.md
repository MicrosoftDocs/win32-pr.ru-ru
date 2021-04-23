---
description: Список кандидатов представляется структурой КАНДИДАТЕЛИСТ, содержащей массив строк, указывающий символы или символьные строки, из которых пользователь может выбрать.
ms.assetid: 7e83e3ee-8a60-4fdd-930b-81f33af8f5bf
title: Списки кандидатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691809638d8ba639538a5bcc887d1db953c053c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547114"
---
# <a name="candidate-lists"></a><span data-ttu-id="cb77f-103">Списки кандидатов</span><span class="sxs-lookup"><span data-stu-id="cb77f-103">Candidate Lists</span></span>

<span data-ttu-id="cb77f-104">Список кандидатов представляется структурой [**кандидателист**](/windows/win32/api/imm/ns-imm-candidatelist) , содержащей массив строк, указывающий символы или символьные строки, из которых пользователь может выбрать.</span><span class="sxs-lookup"><span data-stu-id="cb77f-104">A candidate list is represented by a [**CANDIDATELIST**](/windows/win32/api/imm/ns-imm-candidatelist) structure containing an array of strings specifying the characters or character strings from which the user can choose.</span></span> <span data-ttu-id="cb77f-105">Приложение, поддерживающее IME, может получать сведения списка кандидатов с помощью функций [**иммжеткандидателисткаунт**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) и [**иммжеткандидателист**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) .</span><span class="sxs-lookup"><span data-stu-id="cb77f-105">Your IME-aware application can retrieve candidate list information using the [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) and [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb77f-106">См. также</span><span class="sxs-lookup"><span data-stu-id="cb77f-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb77f-107">О диспетчере методов ввода</span><span class="sxs-lookup"><span data-stu-id="cb77f-107">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



