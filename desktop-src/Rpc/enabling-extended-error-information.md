---
title: Включение расширенных сведений об ошибках
description: Включение расширенных сведений об ошибках для удаленного вызова процедур (RPC).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd6579069c840d8f6dba5a9cd0e0d4edc831f6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258673"
---
# <a name="enabling-extended-error-information"></a><span data-ttu-id="c50bc-103">Включение расширенных сведений об ошибках</span><span class="sxs-lookup"><span data-stu-id="c50bc-103">Enabling Extended Error Information</span></span>

<span data-ttu-id="c50bc-104">Чтобы включить расширенные сведения об ошибке, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c50bc-104">To enable extended error information, take the following steps:</span></span>

<span data-ttu-id="c50bc-105">Откройте политику локального компьютера с помощью интерфейса gpedit. msc.</span><span class="sxs-lookup"><span data-stu-id="c50bc-105">Open the local machine policy using the gpedit.msc interface.</span></span>

<span data-ttu-id="c50bc-106">Перейдите к политике, расположенной в разделе Конфигурация компьютера/административные шаблоны/Система/удаленный вызов процедуры/устранение неполадок RPC, поддержка и распространение расширенных сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="c50bc-106">Navigate to the policy located at Computer Configuration/Administrative Templates/System/Remote Procedure Call/Rpc Troubleshooting Support/Propagation of extended error information</span></span>

<span data-ttu-id="c50bc-107">Включите политику и задайте для поля **распространение расширенных сведений об ошибке** значение "вкл.".</span><span class="sxs-lookup"><span data-stu-id="c50bc-107">Enable the policy, and set the field **Propagation of extended error information** to "On".</span></span>

<span data-ttu-id="c50bc-108">Этот процесс включает распространение расширенных сведений об ошибках для всех процессов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c50bc-108">This process turns the propagation of extended error information on for all processes on the machine.</span></span>

<span data-ttu-id="c50bc-109">Чтобы включить расширенные сведения об ошибках только для определенных процессов на компьютере или отключить его только для определенных процессов на компьютере, используйте параметр **отключить с исключениями** или **включить с помощью исключений** .</span><span class="sxs-lookup"><span data-stu-id="c50bc-109">To enable extended error information for only certain processes on a computer, or to disable it for only certain processes on the computer, use the **Off with exceptions** or **On with exceptions** options.</span></span> <span data-ttu-id="c50bc-110">Оба варианта используют исключения поля **расширенных сведений об ошибках** , чтобы указать, какие процессы имеют значение по умолчанию и какие процессы имеют противоположный параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c50bc-110">Both options use the field **Extended Error Information Exceptions** to specify which processes have the default setting, and which processes have the opposite of the default setting.</span></span> <span data-ttu-id="c50bc-111">**Расширенные исключения сведений об ошибках** содержат список имен процессов.</span><span class="sxs-lookup"><span data-stu-id="c50bc-111">**Extended Error Information Exceptions** contains a list of process names.</span></span>

<span data-ttu-id="c50bc-112">Если командная строка процесса начинается со строки, которая находится в **исключениях расширенных сведений об ошибке**, процесс получит противоположный параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c50bc-112">If the command line of a process starts with a string that is in the **Extended Error Information Exceptions**, the process will receive the opposite of the default setting.</span></span> <span data-ttu-id="c50bc-113">Например, если требуется, чтобы весь процесс на компьютере распространил расширенные сведения об ошибке, за исключением LSASS и процесса, называемого **Secure Server**, задайте для **распространения расширенных сведений об ошибках** значение **вкл**., а в поле **исключений расширенных сведений об ошибках** укажите следующую строку: LSASS "Secure Server".</span><span class="sxs-lookup"><span data-stu-id="c50bc-113">For example, if you want all the process on your computer to propagate extended error information, except for lsass and the process called **Secure Server**, set the **Propagation of extended error information** to **On with exceptions**, and specify in the **Extended Error Information Exceptions** field the following string: lsass "Secure Server".</span></span>

<span data-ttu-id="c50bc-114">Строки можно заключать в двойные кавычки, но это необязательно, если в строке нет пробелов.</span><span class="sxs-lookup"><span data-stu-id="c50bc-114">Strings can be enclosed with double quotes, but doing so is optional if there are no spaces in the string.</span></span> <span data-ttu-id="c50bc-115">Кроме того, можно указать начало командной строки процесса.</span><span class="sxs-lookup"><span data-stu-id="c50bc-115">Also, the beginning of the process command line can be specified.</span></span> <span data-ttu-id="c50bc-116">Например, если параметр **Off с исключениями** указан в поле **распространение расширенных сведений об ошибке** , а в поле **исключения расширенных сведений об ошибках** указано следующее: Win.</span><span class="sxs-lookup"><span data-stu-id="c50bc-116">For example, if **Off with exceptions** is specified in the **Propagation of extended error information** field, and in the **Extended Error Information Exceptions** field the following is specified: win.</span></span>

<span data-ttu-id="c50bc-117">Каждый процесс, начинающийся с "Win", распространяет расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="c50bc-117">Each process that begins with "win" propagates extended error information.</span></span> <span data-ttu-id="c50bc-118">Например, на многих компьютерах эти процессы будут winlogon.exe и WINWORD.EXE.</span><span class="sxs-lookup"><span data-stu-id="c50bc-118">On many computers, for example, those processes would be winlogon.exe and WINWORD.EXE.</span></span>

 

 




