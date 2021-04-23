---
title: Файлы заголовков
description: Файл заголовка интерфейса (Name. h) содержит определения типов и объявления функций на основе определения интерфейса в текущем IDL-файле, а также всех типов данных и операций, объявленных в файлах, включенных в директиву \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- файлы заголовков MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661611"
---
# <a name="the-header-files"></a><span data-ttu-id="c3a5b-104">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c3a5b-104">The Header Files</span></span>

<span data-ttu-id="c3a5b-105">Файл заголовка интерфейса (Name. h) содержит определения типов и объявления функций на основе определения интерфейса в текущем IDL-файле, а также всех типов данных и операций, объявленных в файлах, включенных в \# директиву include.</span><span class="sxs-lookup"><span data-stu-id="c3a5b-105">The interface header file (Name.h) contains type definitions and function declarations based on the interface definition in the current IDL file, as well as all the data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="c3a5b-106">Типы данных из файлов, импортированных с помощью директивы Import, не реплицируются в файл заголовка. Вместо этого созданный файл заголовка содержит строку include для H файла, созданного из импортированного файла.</span><span class="sxs-lookup"><span data-stu-id="c3a5b-106">Data types from the files imported with the import directive are not replicated to the header file; instead, the generated header file contains an include line to the H file generated from the imported file.</span></span>

<span data-ttu-id="c3a5b-107">Включите этот файл в исходные файлы для прокси-библиотеки DLL и клиентских приложений, использующих интерфейс.</span><span class="sxs-lookup"><span data-stu-id="c3a5b-107">Include this file in the source files for the proxy DLL and for client applications that use the interface.</span></span>

<span data-ttu-id="c3a5b-108">Имя по умолчанию для файла заголовка, созданного из файла. idl — File. h.</span><span class="sxs-lookup"><span data-stu-id="c3a5b-108">The default name for a header file generated from a file.idl is File.h.</span></span> <span data-ttu-id="c3a5b-109">Параметр компилятора [**/Header**](-header.md) MIDL переопределяет имя файла заголовка интерфейса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c3a5b-109">The [**/header**](-header.md) MIDL compiler switch overrides the default name of the interface header file.</span></span>

 

 




