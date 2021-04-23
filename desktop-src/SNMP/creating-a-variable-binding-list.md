---
title: Создание списка привязок переменных
description: Функция Снмпкреатевбл создает новый список привязок переменных.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258539"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="1e457-103">Создание списка привязок переменных</span><span class="sxs-lookup"><span data-stu-id="1e457-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="1e457-104">Функция [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) создает новый список привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="1e457-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="1e457-105">Если в приложении WinSNMP указано имя переменной и значение, функция создает список и добавляет имя и значение в качестве первой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="1e457-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="1e457-106">Если в приложении для имени переменной указано **значение NULL** , то функция создает пустой список.</span><span class="sxs-lookup"><span data-stu-id="1e457-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="1e457-107">Чтобы скопировать список привязок переменных, вызовите функцию [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) .</span><span class="sxs-lookup"><span data-stu-id="1e457-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="1e457-108">Функция создает новый список привязок переменных и инициализирует новый список копией данных в списке привязок исходной переменной.</span><span class="sxs-lookup"><span data-stu-id="1e457-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="1e457-109">Функция [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) и функция [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) выделяют любую необходимую память для нового списка привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="1e457-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="1e457-110">В приложении WinSNMP должны освобождаться ресурсы, связанные с этими списками.</span><span class="sxs-lookup"><span data-stu-id="1e457-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="1e457-111">Рекомендуется, чтобы приложение выделило это, сопоставляя каждый вызов [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) и [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) с соответствующим вызовом функции [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) , когда нужно освободить выделенную память.</span><span class="sxs-lookup"><span data-stu-id="1e457-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 




