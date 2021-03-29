---
title: Не доверять одноранговому узлу
description: '\ 0034; не доверяете узлу \ 0034; — Это базовое правило безопасности, но оно часто оказывается незнакомым.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775500"
---
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="9dbc7-103">Не доверять одноранговому узлу</span><span class="sxs-lookup"><span data-stu-id="9dbc7-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="9dbc7-104">"Не доверять одноранговому узлу" — это базовое правило безопасности, но оно часто проявляется.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="9dbc7-105">Не следует предполагать, что другая сторона связи будет работать правильно, и не предполагать, что ваш узел передаст ожидаемые данные.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="9dbc7-106">MIDL и RPC выполняют некоторые проверки от вашего имени, но не все проверки.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="9dbc7-107">Определите, какой аспект параметров проверяется с помощью MIDL или RPC, а также какие аспекты необходимо проверить самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="9dbc7-108">Например, для дескрипторов контекста in и out RPC проверяет дескриптор контекста на недопустимое значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="9dbc7-109">Он допускает значения NULL и допустимые значения, но многие разработчики не знают, что разрешены значения NULL.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="9dbc7-110">Это то, что нужно проверить.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-110">This is something to check for.</span></span>

<span data-ttu-id="9dbc7-111">Даже если вы доверяете одноранговому узлу, не забудьте ввести новые пути, по которым скомпрометированный компьютер или учетная запись участника могут атаковать другие компьютеры.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="9dbc7-112">Представьте, что пользователь выбирает свой день рождения в качестве своего пароля, и он считается злоумышленником.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="9dbc7-113">Даже после того, как запросы пользователя проходят проверку подлинности и разрешен доступ к своим данным, убедитесь, что уязвимые места не существуют, такие переполнения стека, которые могут позволить злоумышленнику взять на себя контроль над вашим сервером и расширить нарушение безопасности.</span><span class="sxs-lookup"><span data-stu-id="9dbc7-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




