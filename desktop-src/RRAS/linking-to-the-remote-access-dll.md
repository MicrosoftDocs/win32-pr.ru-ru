---
title: Связывание с библиотекой DLL удаленного доступа
description: Если приложение связывается статически с DLL-библиотекой RASAPI32, приложение не сможет загрузиться, если служба удаленного доступа не установлена.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890904"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="f56fa-103">Связывание с библиотекой DLL удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="f56fa-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="f56fa-104">Если приложение связывается статически с DLL-библиотекой RASAPI32, приложение не сможет загрузиться, если служба удаленного доступа не установлена.</span><span class="sxs-lookup"><span data-stu-id="f56fa-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="f56fa-105">Приложение RAS может загружаться, когда служба удаленного доступа не установлена с помощью [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) для загрузки библиотеки DLL, а [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) — для получения указателей на функции RAS.</span><span class="sxs-lookup"><span data-stu-id="f56fa-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="f56fa-106">Функции RAS находятся в RASAPI32.DLL.</span><span class="sxs-lookup"><span data-stu-id="f56fa-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="f56fa-107">Библиотека импорта для этих функций — RASAPI32. LIB.</span><span class="sxs-lookup"><span data-stu-id="f56fa-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="f56fa-108">Чтобы использовать функции RAS, программы должны включать следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="f56fa-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="f56fa-109">Файл</span><span class="sxs-lookup"><span data-stu-id="f56fa-109">File</span></span>       | <span data-ttu-id="f56fa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f56fa-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f56fa-111">Соединяющ. Высоты</span><span class="sxs-lookup"><span data-stu-id="f56fa-111">RAS.H</span></span>      | <span data-ttu-id="f56fa-112">Содержит прототипы функций RAS, константы и определения структур.</span><span class="sxs-lookup"><span data-stu-id="f56fa-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="f56fa-113">РАСЕРРОР. Высоты</span><span class="sxs-lookup"><span data-stu-id="f56fa-113">RASERROR.H</span></span> | <span data-ttu-id="f56fa-114">Содержит коды ошибок RAS.</span><span class="sxs-lookup"><span data-stu-id="f56fa-114">Contains the RAS error codes.</span></span>                                               |



 

 

 