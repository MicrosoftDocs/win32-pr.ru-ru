---
description: Протокол PGM использует параметры сокета для задания состояния, предоставления многоадресных параметров и иным образом реализует возможности многоадресной рассылки.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Параметры сокета PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897313"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="ace77-103">Параметры сокета PGM</span><span class="sxs-lookup"><span data-stu-id="ace77-103">PGM Socket Options</span></span>

<span data-ttu-id="ace77-104">Протокол PGM использует параметры сокета для задания состояния, предоставления многоадресных параметров и иным образом реализует возможности многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="ace77-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="ace77-105">На этой странице указывается, как должны быть установлены параметры сокета PGM, перечислены параметры сокета, доступные для протокола PGM, и там, где это необходимо, приведены примеры использования и дополнительные сведения о различных параметрах.</span><span class="sxs-lookup"><span data-stu-id="ace77-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="ace77-106">Базовые определения для каждого параметра сокета PCM см. в разделе [параметры сокета](socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="ace77-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="ace77-107">**Windows XP:** Безопасное многоадресное программирование (PGM) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ace77-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="ace77-108">Для отправителей PGM доступны следующие параметры сокета:</span><span class="sxs-lookup"><span data-stu-id="ace77-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="ace77-109">\_ЛАТЕЖОИН RM</span><span class="sxs-lookup"><span data-stu-id="ace77-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="ace77-110">\_ \_ Размер окна "коэффициент RM" \_</span><span class="sxs-lookup"><span data-stu-id="ace77-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="ace77-111">\_Частота отправки \_ окна \_ диспетчера \_ RM</span><span class="sxs-lookup"><span data-stu-id="ace77-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="ace77-112">\_Статистика отправителя RM \_</span><span class="sxs-lookup"><span data-stu-id="ace77-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="ace77-113">\_ \_ \_ метод аванса окна отправителя RM \_</span><span class="sxs-lookup"><span data-stu-id="ace77-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="ace77-114">RM \_ Set \_ мкаст \_ TTL</span><span class="sxs-lookup"><span data-stu-id="ace77-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="ace77-115">\_ \_ граница сообщения набора \_ RM</span><span class="sxs-lookup"><span data-stu-id="ace77-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="ace77-116">RM \_ Set \_ Send, \_ Если</span><span class="sxs-lookup"><span data-stu-id="ace77-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="ace77-117">RM \_ использует \_ фек</span><span class="sxs-lookup"><span data-stu-id="ace77-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="ace77-118">\_ \_ Параметр метода Advance окна отправителя RM \_ \_ указывает метод, используемый при перемещении окна завершающей пограничной отправки.</span><span class="sxs-lookup"><span data-stu-id="ace77-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="ace77-119">Параметр оптвал может иметь только \_ \_ аванс окна \_ по \_ времени (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ace77-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="ace77-120">Обратите внимание, что \_ \_ Использование окна \_ в качестве \_ \_ кэша данных не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ace77-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="ace77-121">Для приемников PGM доступны следующие параметры сокета:</span><span class="sxs-lookup"><span data-stu-id="ace77-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="ace77-122">\_Добавить \_ Получение, \_ Если</span><span class="sxs-lookup"><span data-stu-id="ace77-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="ace77-123">RM \_ Del \_ Receive, \_ Если</span><span class="sxs-lookup"><span data-stu-id="ace77-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="ace77-124">\_Высокая скорость работы в \_ \_ ИНТРАСЕТи (RM) \_</span><span class="sxs-lookup"><span data-stu-id="ace77-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="ace77-125">\_Статистика приемника RM \_</span><span class="sxs-lookup"><span data-stu-id="ace77-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="ace77-126">Настройка параметров сокета PGM</span><span class="sxs-lookup"><span data-stu-id="ace77-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="ace77-127">В следующем фрагменте кода показано руководство по программированию для настройки параметров сокета PGM:</span><span class="sxs-lookup"><span data-stu-id="ace77-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="ace77-128">В приведенном выше фрагменте тип и содержимое *оптиондата* зависят от устанавливаемого параметра сокета.</span><span class="sxs-lookup"><span data-stu-id="ace77-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="ace77-129">Для всех параметров сокета PGM используется уровень сокета ИППРОТО \_ RM.</span><span class="sxs-lookup"><span data-stu-id="ace77-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="ace77-130">Параметры сокета PGM должны быть установлены сразу после вызова функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) со следующими исключениями:</span><span class="sxs-lookup"><span data-stu-id="ace77-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="ace77-131">\_ \_ граница сообщения набора \_ RM</span><span class="sxs-lookup"><span data-stu-id="ace77-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="ace77-132">\_Статистика отправителя RM \_</span><span class="sxs-lookup"><span data-stu-id="ace77-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="ace77-133">\_Статистика приемника RM \_</span><span class="sxs-lookup"><span data-stu-id="ace77-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



