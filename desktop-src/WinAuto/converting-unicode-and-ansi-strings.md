---
title: Преобразование строк Юникода и ANSI
description: Microsoft Active Accessibility использует строки в Юникоде, как определено типом данных BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338340"
---
# <a name="converting-unicode-and-ansi-strings"></a><span data-ttu-id="6d766-103">Преобразование строк Юникода и ANSI</span><span class="sxs-lookup"><span data-stu-id="6d766-103">Converting Unicode and ANSI Strings</span></span>

<span data-ttu-id="6d766-104">Microsoft Active Accessibility использует строки в Юникоде, как определено типом данных **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="6d766-104">Microsoft Active Accessibility uses Unicode strings as defined by the **BSTR** data type.</span></span> <span data-ttu-id="6d766-105">Если приложение не использует строки в Юникоде или вы хотите преобразовать строки для определенных вызовов API, используйте функции Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) и [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) для выполнения необходимого преобразования.</span><span class="sxs-lookup"><span data-stu-id="6d766-105">If your application does not use Unicode strings, or if you want to convert strings for certain API calls, use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) Microsoft Win32 functions to perform the necessary conversion.</span></span>

<span data-ttu-id="6d766-106">Используйте [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) для преобразования строки Юникода в строку ANSI.</span><span class="sxs-lookup"><span data-stu-id="6d766-106">Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) to convert a Unicode string to an ANSI string.</span></span> <span data-ttu-id="6d766-107">Функция [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) ПРЕОБРАЗУЕТ строку ANSI в строку Юникода.</span><span class="sxs-lookup"><span data-stu-id="6d766-107">The [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function converts an ANSI string to a Unicode string.</span></span>

<span data-ttu-id="6d766-108">Используйте [**сисаллокстринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) и [**сисфристринг**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) для выделения и освобождения типов данных **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="6d766-108">Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) to allocate and free **BSTR** data types.</span></span>

<span data-ttu-id="6d766-109">Дополнительные сведения об этих строковых функциях см. в разделе ссылки в пакете средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="6d766-109">For more information about these string functions, see their references in the Windows Software Development Kit (SDK).</span></span>

 

 