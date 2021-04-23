---
description: В контексте, ориентированном на соединение, вызывающая функция отвечает за форматирование сообщений. Вызывающий объект использует пакет безопасности для проверки подлинности подключений и обеспечения целостности отдельных частей сообщения.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Контексты Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155899"
---
# <a name="connection-oriented-contexts"></a><span data-ttu-id="abc3a-104">Контексты Connection-Oriented</span><span class="sxs-lookup"><span data-stu-id="abc3a-104">Connection-Oriented Contexts</span></span>

<span data-ttu-id="abc3a-105">В [*контексте*](/windows/desktop/SecGloss/c-gly), ориентированном на соединение, вызывающая функция отвечает за форматирование сообщений.</span><span class="sxs-lookup"><span data-stu-id="abc3a-105">With a connection-oriented [*context*](/windows/desktop/SecGloss/c-gly), the function's caller is responsible for formatting messages.</span></span> <span data-ttu-id="abc3a-106">Вызывающий объект использует [*пакет безопасности*](/windows/desktop/SecGloss/s-gly) для проверки подлинности подключений и обеспечения целостности отдельных частей сообщения.</span><span class="sxs-lookup"><span data-stu-id="abc3a-106">The caller relies on the [*security package*](/windows/desktop/SecGloss/s-gly) to authenticate connections and to ensure the integrity of specific parts of the message.</span></span>

<span data-ttu-id="abc3a-107">Большинство контекстных параметров доступны для контекстов, ориентированных на соединение.</span><span class="sxs-lookup"><span data-stu-id="abc3a-107">Most context options are available to connection-oriented contexts.</span></span> <span data-ttu-id="abc3a-108">Эти параметры включают взаимную проверку подлинности, обнаружение воспроизведения и обнаружение последовательности, как описано в разделе [требования к контексту](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="abc3a-108">These options include mutual authentication, replay detection, and sequence detection, as described in [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="abc3a-109">Пакет безопасности устанавливает \_ флаг подключения флага SECPKG, \_ чтобы указать, что он поддерживает семантику, ориентированную на соединение.</span><span class="sxs-lookup"><span data-stu-id="abc3a-109">A security package sets the SECPKG\_FLAG\_CONNECTION flag to indicate that it supports connection-oriented semantics.</span></span>

 

 
