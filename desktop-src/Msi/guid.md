---
description: Тип данных GUID — это текстовая строка, представляющая идентификатор класса (ID). COM должен иметь возможность преобразовать строку в допустимый идентификатор класса. Все идентификаторы GUID должны быть созданы в верхнем регистре.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663691"
---
# <a name="guid"></a><span data-ttu-id="bf44b-105">Код GUID</span><span class="sxs-lookup"><span data-stu-id="bf44b-105">GUID</span></span>

<span data-ttu-id="bf44b-106">Тип данных GUID — это текстовая строка, представляющая идентификатор класса (ID).</span><span class="sxs-lookup"><span data-stu-id="bf44b-106">The GUID data type is a text string representing a Class identifier (ID).</span></span> <span data-ttu-id="bf44b-107">COM должен иметь возможность преобразовать строку в допустимый идентификатор класса.</span><span class="sxs-lookup"><span data-stu-id="bf44b-107">COM must be able to convert the string to a valid Class ID.</span></span> <span data-ttu-id="bf44b-108">Все идентификаторы GUID должны быть созданы в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="bf44b-108">All GUIDs must be authored in uppercase.</span></span>

<span data-ttu-id="bf44b-109">Допустимым форматом для GUID является {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, где X — шестнадцатеричная цифра (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F).</span><span class="sxs-lookup"><span data-stu-id="bf44b-109">The valid format for a GUID is {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} where X is a hex digit (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).</span></span>

<span data-ttu-id="bf44b-110">Обратите внимание, что такие программы, как GUIDGEN, могут создавать идентификаторы GUID, содержащие строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="bf44b-110">Note that utilities such as GUIDGEN can generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="bf44b-111">Все эти имена должны быть заменены на прописные, прежде чем идентификатор GUID может быть использован установщиком в качестве допустимого кода продукта, кода пакета или кода компонента.</span><span class="sxs-lookup"><span data-stu-id="bf44b-111">These must all be changed to uppercase letters before the GUID can be used by the installer as a valid product code, package code, or component code.</span></span>

 

 



