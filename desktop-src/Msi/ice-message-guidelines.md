---
description: Пользовательские действия ICE взаимодействуют путем вызова Мсипроцессмессаже и отправки \_ сообщения инсталлмессаже типа пользователя.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Рекомендации по сообщениям ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991074"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="cfc4a-103">Рекомендации по сообщениям ICE</span><span class="sxs-lookup"><span data-stu-id="cfc4a-103">ICE Message Guidelines</span></span>

<span data-ttu-id="cfc4a-104">Пользовательские действия ICE взаимодействуют путем вызова [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) и отправки \_ сообщения инсталлмессаже типа пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="cfc4a-105">При создании строки сообщения для пользовательского действия ICE отформатируйте строку следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="cfc4a-106">*Имя Ice* <tab> *Тип сообщения* <tab> *Описание* <tab> *URL-адрес справки или расположение* <tab> *Имя таблицы* <tab> *Имя столбца* <tab> *Первичный ключ* <tab> *Первичный ключ* <tab> *Первичный ключ* .</span><span class="sxs-lookup"><span data-stu-id="cfc4a-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="cfc4a-107">.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-107">.</span></span> <span data-ttu-id="cfc4a-108">.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-108">.</span></span> <span data-ttu-id="cfc4a-109">(повторять для любого необходимого количества первичных ключей)</span><span class="sxs-lookup"><span data-stu-id="cfc4a-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="cfc4a-110">Первые три поля строки обязательны в каждом сообщении.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="cfc4a-111">В поле Тип сообщения указывается, сообщает ли ICE о сбое, ошибке, предупреждении или информационном сообщении.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="cfc4a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc4a-112">Value</span></span> | <span data-ttu-id="cfc4a-113">Тип сообщения</span><span class="sxs-lookup"><span data-stu-id="cfc4a-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc4a-114">0</span><span class="sxs-lookup"><span data-stu-id="cfc4a-114">0</span></span>     | <span data-ttu-id="cfc4a-115">Сообщение об ошибке, сообщающее о сбое настраиваемого действия ICE.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="cfc4a-116">1</span><span class="sxs-lookup"><span data-stu-id="cfc4a-116">1</span></span>     | <span data-ttu-id="cfc4a-117">Сообщение об ошибке создания отчетов, которое вызывает неправильное поведение.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="cfc4a-118">2</span><span class="sxs-lookup"><span data-stu-id="cfc4a-118">2</span></span>     | <span data-ttu-id="cfc4a-119">Предупреждающее сообщение создание отчетов о базе данных, которое приводит к неправильному поведению в некоторых случаях.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="cfc4a-120">Предупреждения также могут сообщать о непредвиденных побочных эффектах создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="cfc4a-121">3</span><span class="sxs-lookup"><span data-stu-id="cfc4a-121">3</span></span>     | <span data-ttu-id="cfc4a-122">Информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="cfc4a-123">Если справка недоступна, в поле URL-адрес справки может быть указана пустая строка.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="cfc4a-124">Сообщения об ошибках и предупреждения должны указывать поля имя таблицы, имя столбца и первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="cfc4a-125">Если любое из этих полей пропущено, все поля, следующие за первым пустым полем, должны остаться в сообщении.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="cfc4a-126">Например, имя таблицы предоставляется без имени столбца, первичных ключей или имени таблицы, а имя столбца не предоставляется без первичных ключей.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="cfc4a-127">Однако имя столбца и первичные ключи нельзя использовать без имени таблицы.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="cfc4a-128">Несколько первичных ключей могут быть перечислены до тех пор, пока не будут заданы значения всех первичных ключей в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="cfc4a-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="cfc4a-129">Examples</span></span>

<span data-ttu-id="cfc4a-130">Первое сообщение, показанное в [образце Ice в C++](sample-ice-in-c-.md):</span><span class="sxs-lookup"><span data-stu-id="cfc4a-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="cfc4a-131">"ICE01 \\ T3 \\ ткреатед 04/29/1998, <вставить имя автора>".</span><span class="sxs-lookup"><span data-stu-id="cfc4a-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="cfc4a-132">Второе сообщение, опубликованное образцом ICE:</span><span class="sxs-lookup"><span data-stu-id="cfc4a-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="cfc4a-133">"ICE01 \\ T3 \\ тласт изменил 05/06/1999, <вставить имя автора>".</span><span class="sxs-lookup"><span data-stu-id="cfc4a-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="cfc4a-134">Третье сообщение, размещенное в образце ICE.</span><span class="sxs-lookup"><span data-stu-id="cfc4a-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="cfc4a-135">"ICE01 \\ T3 \\ тсимпле, чтобы продемонстрировать концепцию Ice".</span><span class="sxs-lookup"><span data-stu-id="cfc4a-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



