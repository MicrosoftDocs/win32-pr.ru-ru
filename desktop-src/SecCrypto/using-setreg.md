---
description: Инструмент SetReg задает значение разделов реестра, определяющих поведение процесса проверки сертификата Authenticode.
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: Использование SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155083"
---
# <a name="using-setreg"></a><span data-ttu-id="a9a0c-103">Использование SetReg</span><span class="sxs-lookup"><span data-stu-id="a9a0c-103">Using SetReg</span></span>

<span data-ttu-id="a9a0c-104">Инструмент SetReg задает значение разделов реестра, определяющих поведение процесса проверки сертификата Authenticode.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="a9a0c-105">Эти ключи, называемые ключами состояния публикации программного обеспечения, определяют, следует ли доверять тестовому корню, разрешать автономное утверждение сертификатов, проверять сроки действия сертификатов и выполнять проверки отзыва.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="a9a0c-106">Следующая команда перечисляет синтаксис и параметры для использования SetReg.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="a9a0c-107">**Setreg-?**</span><span class="sxs-lookup"><span data-stu-id="a9a0c-107">**setreg -?**</span></span>

<span data-ttu-id="a9a0c-108">Следующая команда делает тест корневым доверенным.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="a9a0c-109">По умолчанию тестовый корень не является доверенным.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="a9a0c-110">После внесения любых изменений в значения ключей отображается список текущего значения всех ключевых значений.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="a9a0c-111">Если используется параметр **-q** , значения ключа не отображаются.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="a9a0c-112">**Setreg 1 TRUE**</span><span class="sxs-lookup"><span data-stu-id="a9a0c-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="a9a0c-113">Следующая команда делает тестовый корень ненадежным и вызывает проверку на наличие отзыва.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="a9a0c-114">Параметр **-q** используется, чтобы список значений ключей не отображался.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="a9a0c-115">**Setreg-q 1 FALSE 3 TRUE**</span><span class="sxs-lookup"><span data-stu-id="a9a0c-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="a9a0c-116">Команды, параметры и аргументы не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="a9a0c-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



