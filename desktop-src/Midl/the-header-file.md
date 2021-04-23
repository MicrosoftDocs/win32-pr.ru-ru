---
title: Файл заголовка
description: Файл заголовка содержит определения всех типов данных и операций, объявленных в IDL-файле, а также все типы данных и операции, объявленные в файлах, включенных в директиву \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL и RPC MIDL, интерфейсы, заголовочный файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068309"
---
# <a name="the-header-file"></a><span data-ttu-id="b984c-104">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="b984c-104">The Header File</span></span>

<span data-ttu-id="b984c-105">Файл заголовка содержит определения всех типов данных и операций, объявленных в IDL-файле, а также все типы данных и операции, объявленные в файлах, включенных в \# директиву include.</span><span class="sxs-lookup"><span data-stu-id="b984c-105">The header file contains definitions of all data types and operations declared in the IDL file, as well as all data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="b984c-106">Типы данных из файлов, импортированных с помощью директивы Import, не реплицируются в файл заголовка. Вместо этого созданный файл заголовка содержит строку include для H файла, созданного из импортированного файла.</span><span class="sxs-lookup"><span data-stu-id="b984c-106">Data types from the files imported with the import directive are not replicated to the header file; instead the generated header file contains an include line to the H file generated from the imported file.</span></span> <span data-ttu-id="b984c-107">Файл заголовка должен включаться во все модули приложений, вызывающие определенные операции, реализовывать определенные операции или манипулировать определенными типами.</span><span class="sxs-lookup"><span data-stu-id="b984c-107">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="b984c-108">Компилятор MIDL переключает [**/Header**](-header.md) и [**/out**](-out.md) на файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="b984c-108">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




