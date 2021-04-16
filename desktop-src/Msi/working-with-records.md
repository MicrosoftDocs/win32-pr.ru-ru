---
description: Установщик предоставляет функции, которые управляют записями в базе данных установки. Эти функции можно использовать совместно с функциями, описанными в разделе Работа с запросами для внесения фактических изменений в базу данных.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Работа с записями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650888"
---
# <a name="working-with-records"></a><span data-ttu-id="db444-104">Работа с записями</span><span class="sxs-lookup"><span data-stu-id="db444-104">Working with Records</span></span>

<span data-ttu-id="db444-105">Установщик предоставляет функции, которые управляют записями в базе данных установки.</span><span class="sxs-lookup"><span data-stu-id="db444-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="db444-106">Эти функции можно использовать совместно с функциями, описанными в разделе [Работа с запросами](working-with-queries.md) для внесения фактических изменений в базу данных.</span><span class="sxs-lookup"><span data-stu-id="db444-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="db444-107">Следующие функции создают или удаляют записи:</span><span class="sxs-lookup"><span data-stu-id="db444-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="db444-108">Чтобы создать новую запись для базы данных, вызовите функцию [**мсикреатерекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .</span><span class="sxs-lookup"><span data-stu-id="db444-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="db444-109">Чтобы очистить данные из записи, присвойте каждому полю значение null, вызвав функцию [**мсирекордклеардата**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .</span><span class="sxs-lookup"><span data-stu-id="db444-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="db444-110">Указанные поля записей заполняются следующими функциями:</span><span class="sxs-lookup"><span data-stu-id="db444-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="db444-111">Чтобы задать запись в целое число, вызовите функцию [**мсирекордсетинтежер**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .</span><span class="sxs-lookup"><span data-stu-id="db444-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="db444-112">Чтобы задать запись в строку, вызовите функцию [**мсирекордсетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .</span><span class="sxs-lookup"><span data-stu-id="db444-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="db444-113">Чтобы вставить весь файл в поле потока, вызовите функцию [**мсирекордсетстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .</span><span class="sxs-lookup"><span data-stu-id="db444-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="db444-114">Следующие функции считывают значения из указанных полей записей:</span><span class="sxs-lookup"><span data-stu-id="db444-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="db444-115">Чтобы считать целочисленное значение из поля, вызовите функцию [**мсирекорджетинтежер**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .</span><span class="sxs-lookup"><span data-stu-id="db444-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="db444-116">Чтобы получить строковое значение, вызовите функцию [**мсирекорджетстринг**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .</span><span class="sxs-lookup"><span data-stu-id="db444-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="db444-117">Чтобы получить поток, вызовите функцию [**мсирекордреадстреам**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .</span><span class="sxs-lookup"><span data-stu-id="db444-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="db444-118">Чтобы определить, имеет ли определенное поле записи значение null, вызовите функцию [**мсирекордиснулл**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .</span><span class="sxs-lookup"><span data-stu-id="db444-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="db444-119">Следующие функции являются информационными функциями записи.</span><span class="sxs-lookup"><span data-stu-id="db444-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="db444-120">Чтобы получить число полей, содержащихся в записи, вызовите функцию [**мсирекорджетфиелдкаунт**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .</span><span class="sxs-lookup"><span data-stu-id="db444-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="db444-121">Чтобы получить размер поля, вызовите функцию [**мсирекорддатасизе**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) .</span><span class="sxs-lookup"><span data-stu-id="db444-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="db444-122">Возвращаемое значение **мсирекорддатасизе** чувствительно к типу поля.</span><span class="sxs-lookup"><span data-stu-id="db444-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



