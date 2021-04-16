---
description: В переданном наборе указываются протоколы, которые следуют за протоколом. Средство синтаксического анализа использует переданный набор, только если средство синтаксического анализа может определить следующий протокол из данных в экземпляре протокола.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Указание переданного набора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682902"
---
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="68964-104">Указание переданного набора</span><span class="sxs-lookup"><span data-stu-id="68964-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="68964-105">В переданном наборе указываются протоколы, которые следуют за протоколом.</span><span class="sxs-lookup"><span data-stu-id="68964-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="68964-106">Средство синтаксического анализа использует переданный набор, только если средство синтаксического анализа может определить следующий протокол из данных в экземпляре протокола.</span><span class="sxs-lookup"><span data-stu-id="68964-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="68964-107">Например, протокол TCP имеет свойство Port, определяющее протокол, который следует за протоколом TCP.</span><span class="sxs-lookup"><span data-stu-id="68964-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="68964-108">Значение свойства, равное 20, указывает, что следующий протокол — FTP.</span><span class="sxs-lookup"><span data-stu-id="68964-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="68964-109">Значение свойства 53 указывает на то, что следующий протокол является DNS.</span><span class="sxs-lookup"><span data-stu-id="68964-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="68964-110">Так как свойство Port определяет протокол, следующий за ним, средство синтаксического анализа TCP может использовать следующий заданный набор для получения маркера для протокола, заданного свойством Port.</span><span class="sxs-lookup"><span data-stu-id="68964-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

<span data-ttu-id="68964-111">Передающее наборы хранятся в INI-файле средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="68964-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="68964-112">Например, предыдущий переданный TCP-набор находится в файле tcpip.ini.</span><span class="sxs-lookup"><span data-stu-id="68964-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="68964-113">Обратите внимание, что если библиотека DLL средства синтаксического анализа поддерживает несколько протоколов, каждое средство синтаксического анализа, использующее этот набор, имеет собственное расположение в INI-файле.</span><span class="sxs-lookup"><span data-stu-id="68964-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="68964-114">Сведения о передаче задаются во время реализации функции [**парсераутоинсталлинфо**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="68964-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="68964-115">Средство синтаксического анализа может указывать протоколы, которые предшествуют протоколу синтаксического анализа, и протоколы, которые следуют за протоколом анализатора.</span><span class="sxs-lookup"><span data-stu-id="68964-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="68964-116">Сетевой монитор принимает все протоколы, предшествующие, и добавляет протокол синтаксического анализатора в разделы "Section" в INI-файле средства синтаксического анализа — для каждого предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="68964-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="68964-117">Сетевой монитор сохраняет список протоколов, которые следуют в разделе "набираемый набор" INI-файла средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="68964-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="68964-118">Сетевой монитор сохраняет сведения о переданных наборе в INI-файле средства синтаксического анализа, но средство синтаксического анализа не обращается к INI-файлам напрямую.</span><span class="sxs-lookup"><span data-stu-id="68964-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="68964-119">Чтобы использовать сведения из этого набора, средство синтаксического анализа вызывает функцию [**креатехандоффтабле**](createhandofftable.md) для создания таблицы передачи.</span><span class="sxs-lookup"><span data-stu-id="68964-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="68964-120">Как правило, таблица передачи создается, когда средство синтаксического анализа регистрирует протокол.</span><span class="sxs-lookup"><span data-stu-id="68964-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="68964-121">После регистрации протокола сетевой монитор создает таблицу набираемых наборов, которую может использовать анализатор.</span><span class="sxs-lookup"><span data-stu-id="68964-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="68964-122">При распознавании данных синтаксический анализатор использует его набираемый набор.</span><span class="sxs-lookup"><span data-stu-id="68964-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="68964-123">Сначала средство синтаксического анализа считывает значение свойства, идентифицирующего следующий протокол.</span><span class="sxs-lookup"><span data-stu-id="68964-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="68964-124">Затем средство синтаксического анализа вызывает [**жетпротоколфромтабле**](getprotocolfromtable.md) для получения маркера для следующего протокола.</span><span class="sxs-lookup"><span data-stu-id="68964-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="68964-125">Наконец, средство синтаксического анализа возвращает указатель на маркер в параметре *фнекстпротокол* объекта [**рекогнизефраме**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="68964-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 



