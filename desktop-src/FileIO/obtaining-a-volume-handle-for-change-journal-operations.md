---
description: 'Чтобы получить маркер для тома, который будет использоваться с операциями с журналом изменений (USN), вызовите функцию CreateFile с параметром Лпфиленаме, для которого задана строка следующего вида: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Получение маркера тома для операций журнала изменений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664603"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a><span data-ttu-id="327db-103">Получение маркера тома для операций журнала изменений</span><span class="sxs-lookup"><span data-stu-id="327db-103">Obtaining a Volume Handle for Change Journal Operations</span></span>

<span data-ttu-id="327db-104">Чтобы получить маркер для тома, который будет использоваться с операциями с журналом изменений (USN), вызовите функцию [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с параметром *лпфиленаме* , для которого задана строка следующего вида: \\ \\ . \\ *X*:</span><span class="sxs-lookup"><span data-stu-id="327db-104">To obtain a handle to a volume for use with update sequence number (USN) change journal operations, call the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the *lpFileName* parameter set to a string of the following form: \\\\.\\*X*:</span></span>

<span data-ttu-id="327db-105">Обратите внимание, что *X* — это буква, идентифицирующая диск, на котором отображается том NTFS.</span><span class="sxs-lookup"><span data-stu-id="327db-105">Note that *X* is the letter that identifies the drive on which the NTFS volume appears.</span></span>

<span data-ttu-id="327db-106">Если у тома нет буквы диска, используйте синтаксис, описанный в разделе [именование тома](naming-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="327db-106">If the volume does not have a drive letter, use the syntax described in [Naming a Volume](naming-a-volume.md).</span></span>

 

 



