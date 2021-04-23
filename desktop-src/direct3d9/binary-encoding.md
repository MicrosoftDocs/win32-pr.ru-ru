---
description: В этом разделе описывается двоичная версия формата файла DirectX (. x), представленная в выпуске DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Двоичное кодирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710690"
---
# <a name="binary-encoding"></a><span data-ttu-id="c76ea-103">Двоичное кодирование</span><span class="sxs-lookup"><span data-stu-id="c76ea-103">Binary Encoding</span></span>

<span data-ttu-id="c76ea-104">В этом разделе описывается двоичная версия формата файла DirectX (. x), представленная в выпуске DirectX 3,0.</span><span class="sxs-lookup"><span data-stu-id="c76ea-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="c76ea-105">Двоичный формат представляет собой лексическое представление текстового формата.</span><span class="sxs-lookup"><span data-stu-id="c76ea-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="c76ea-106">Маркеры могут быть изолированными или сопровождаться простыми записями данных.</span><span class="sxs-lookup"><span data-stu-id="c76ea-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="c76ea-107">Изолированные токены предоставляют грамматические структуры, а токены для чтения и записи предоставляют необходимые данные.</span><span class="sxs-lookup"><span data-stu-id="c76ea-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="c76ea-108">Обратите внимание, что все данные хранятся в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="c76ea-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="c76ea-109">Допустимый поток двоичных данных состоит из заголовка, за которым следуют шаблоны и (или) объекты данных.</span><span class="sxs-lookup"><span data-stu-id="c76ea-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="c76ea-110">В этом разделе обсуждаются следующие компоненты формата двоичного файла и приводится пример шаблона и двоичного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="c76ea-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="c76ea-111">Header</span><span class="sxs-lookup"><span data-stu-id="c76ea-111">Header</span></span>](header.md)
-   [<span data-ttu-id="c76ea-112">Лексемы</span><span class="sxs-lookup"><span data-stu-id="c76ea-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="c76ea-113">Записи маркеров</span><span class="sxs-lookup"><span data-stu-id="c76ea-113">Token Records</span></span>](token-records.md)
-   [<span data-ttu-id="c76ea-114">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="c76ea-114">Templates</span></span>](dx9-graphics-reference-x-file-binaryencoding-templates.md)
-   [<span data-ttu-id="c76ea-115">Data</span><span class="sxs-lookup"><span data-stu-id="c76ea-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="c76ea-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="c76ea-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="c76ea-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c76ea-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c76ea-118">Справочник по формату файла X</span><span class="sxs-lookup"><span data-stu-id="c76ea-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



