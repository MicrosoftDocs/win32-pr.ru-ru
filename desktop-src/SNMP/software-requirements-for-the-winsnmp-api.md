---
title: Требования к программному обеспечению для API WinSNMP
description: Приложение WinSNMP должно получить доступ к WinSNMP API через библиотеку динамической компоновки WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252746"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="44eca-103">Требования к программному обеспечению для API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44eca-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="44eca-104">Приложение WinSNMP должно получить доступ к WinSNMP API через библиотеку динамической компоновки WSNMP32.DLL.</span><span class="sxs-lookup"><span data-stu-id="44eca-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="44eca-105">Следующие файлы необходимы для поддержки функций API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="44eca-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="44eca-106">Имя файла</span><span class="sxs-lookup"><span data-stu-id="44eca-106">Filename</span></span>     | <span data-ttu-id="44eca-107">Описание</span><span class="sxs-lookup"><span data-stu-id="44eca-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="44eca-108">WSNMP32. LIB</span><span class="sxs-lookup"><span data-stu-id="44eca-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="44eca-109">Библиотека WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44eca-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="44eca-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="44eca-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="44eca-111">Предоставляет WinSNMP Interface</span><span class="sxs-lookup"><span data-stu-id="44eca-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="44eca-112">WINSNMP. Высоты</span><span class="sxs-lookup"><span data-stu-id="44eca-112">WINSNMP.H</span></span>    | <span data-ttu-id="44eca-113">Файл заголовка WinSNMP</span><span class="sxs-lookup"><span data-stu-id="44eca-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="44eca-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="44eca-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="44eca-115">Получает SNMP-ловушки и перенаправляет их в MGMTAPI.DLL, библиотеку API диспетчера Microsoft SNMP</span><span class="sxs-lookup"><span data-stu-id="44eca-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="44eca-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="44eca-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="44eca-117">Предоставляет служебные программы SNMP</span><span class="sxs-lookup"><span data-stu-id="44eca-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




