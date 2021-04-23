---
description: Библиотека DLL распознавателя должна быть зарегистрирована для использования платформой Tablet PC. Распознаватель должен внести следующие изменения в реестр при установке.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Регистрация библиотеки DLL распознавателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547058"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="38866-104">Регистрация библиотеки DLL распознавателя</span><span class="sxs-lookup"><span data-stu-id="38866-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="38866-105">Библиотека DLL распознавателя должна быть зарегистрирована для использования платформой Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="38866-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="38866-106">Распознаватель должен внести следующие изменения в реестр при установке.</span><span class="sxs-lookup"><span data-stu-id="38866-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="38866-107">Добавьте новый ключ для каждого из идентификаторов CLSID распознавателя в разделе HKEY \_ Local \_ Machine/Software/Microsoft/ТПГ/распознаватели/реестра.</span><span class="sxs-lookup"><span data-stu-id="38866-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="38866-108">Добавьте один CLSID для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="38866-108">Add one CLSID per language.</span></span> <span data-ttu-id="38866-109">В следующей таблице описаны значения, которые должны быть добавлены под каждым из ключей, содержащих идентификаторы CLSID.</span><span class="sxs-lookup"><span data-stu-id="38866-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="38866-110">В именах этих значений учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="38866-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="38866-111">Имя значения</span><span class="sxs-lookup"><span data-stu-id="38866-111">Value name</span></span>                             | <span data-ttu-id="38866-112">Тип значения</span><span class="sxs-lookup"><span data-stu-id="38866-112">Value type</span></span>             | <span data-ttu-id="38866-113">Описание значения</span><span class="sxs-lookup"><span data-stu-id="38866-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38866-114">Флаги возможностей распознавателя</span><span class="sxs-lookup"><span data-stu-id="38866-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="38866-115">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="38866-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="38866-116">DWORD, используемый для определения возможностей распознавателя.</span><span class="sxs-lookup"><span data-stu-id="38866-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="38866-117">Библиотека DLL распознавателя</span><span class="sxs-lookup"><span data-stu-id="38866-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="38866-118">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="38866-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="38866-119">Полный путь к установленной библиотеке DLL распознавателя.</span><span class="sxs-lookup"><span data-stu-id="38866-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="38866-120">Распознаваемые языки</span><span class="sxs-lookup"><span data-stu-id="38866-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="38866-121">\_двоичный файл REG</span><span class="sxs-lookup"><span data-stu-id="38866-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="38866-122">Двоичный массив, описывающий язык или языки, с которыми будет работать распознаватель.</span><span class="sxs-lookup"><span data-stu-id="38866-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="38866-123">В параметре переctype. h \_ определяется максимальное число языков, поддерживаемое распознавателем, и каждый язык берет слово для хранения в элементе «распознаваемые языки».</span><span class="sxs-lookup"><span data-stu-id="38866-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="38866-124">Размер \_ записи реестра binary reg должен быть РАВЕН Max \_ Languages \* sizeof (Word).</span><span class="sxs-lookup"><span data-stu-id="38866-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




