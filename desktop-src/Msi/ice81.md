---
description: ICE81 проверяет таблицу Мсидигиталцертификате, таблицу Мсидигиталсигнатуре, таблицу Мсипатчцертификате и таблицу Мсипаккажецертификате.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810744"
---
# <a name="ice81"></a><span data-ttu-id="e4a66-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="e4a66-103">ICE81</span></span>

<span data-ttu-id="e4a66-104">ICE81 проверяет [таблицу мсидигиталцертификате](msidigitalcertificate-table.md), таблицу [мсидигиталсигнатуре](msidigitalsignature-table.md), таблицу [мсипатчцертификате](msipatchcertificate-table.md)и [таблицу мсипаккажецертификате](msipackagecertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4a66-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="e4a66-105">Это настраиваемое действие ICE отправляет предупреждения для цифровых сертификатов, которые не являются неиспользуемыми или неиспользованными, и отправляет сообщение об ошибке, если подписанный объект не существует или если CAB-файл подписанного объекта не указывает на внешние данные.</span><span class="sxs-lookup"><span data-stu-id="e4a66-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="e4a66-106">Обратите внимание, что ICE03 проверяет, что запись в столбце таблицы в таблице Мсидигиталсигнатуре имеет значение "Media".</span><span class="sxs-lookup"><span data-stu-id="e4a66-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="e4a66-107">Результат</span><span class="sxs-lookup"><span data-stu-id="e4a66-107">Result</span></span>

<span data-ttu-id="e4a66-108">ICE81 отправляет следующие предупреждения для неиспользуемых или неиспользованных цифровых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e4a66-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="e4a66-109">Предупреждение ICE81</span><span class="sxs-lookup"><span data-stu-id="e4a66-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="e4a66-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e4a66-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e4a66-111">Не удается найти ссылку на какие либо записи в таблице Мсидигиталцертификате в таблицах Мсидигиталсигнатуре, Мсипаккажецертификате или Мсипатчцертификате.</span><span class="sxs-lookup"><span data-stu-id="e4a66-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="e4a66-112">Это предупреждение возвращается, если все записи не используются.</span><span class="sxs-lookup"><span data-stu-id="e4a66-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="e4a66-113">Не удалось найти ссылку на цифровой сертификат \[ 1 \] в таблицах Мсидигиталсигнатуре, Мсипаккажецертификате или мсипатчцертификате.</span><span class="sxs-lookup"><span data-stu-id="e4a66-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="e4a66-114">Это предупреждение возвращается, если некоторые записи, но не все, не используются.</span><span class="sxs-lookup"><span data-stu-id="e4a66-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="e4a66-115">ICE81 отправляет следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="e4a66-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="e4a66-116">ICE81, ошибка</span><span class="sxs-lookup"><span data-stu-id="e4a66-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="e4a66-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e4a66-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a66-118">Таблица мультимедиа не существует.</span><span class="sxs-lookup"><span data-stu-id="e4a66-118">Media Table does not exist.</span></span> <span data-ttu-id="e4a66-119">Поэтому все записи в Мсидигиталсигнатуре неверны</span><span class="sxs-lookup"><span data-stu-id="e4a66-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="e4a66-120">Подписанный объект не существует.</span><span class="sxs-lookup"><span data-stu-id="e4a66-120">The signed object does not exist.</span></span> <span data-ttu-id="e4a66-121">Эта ошибка возвращается, если таблица мультимедиа не существует, но Мсидигиталсигнатуре содержит записи.</span><span class="sxs-lookup"><span data-stu-id="e4a66-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="e4a66-122">Отсутствует подписанный объект \[ 2 \] в таблице Media</span><span class="sxs-lookup"><span data-stu-id="e4a66-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="e4a66-123">Подписанный объект \[ 2 \] не существует.</span><span class="sxs-lookup"><span data-stu-id="e4a66-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="e4a66-124">Эта ошибка возвращается, если таблица мультимедиа существует, но эта запись в Мсидигиталсигнатуре отсутствует в таблице Media.</span><span class="sxs-lookup"><span data-stu-id="e4a66-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="e4a66-125">Запись в таблице \[ 1 \] с ключом \[ 2 \] подписана.</span><span class="sxs-lookup"><span data-stu-id="e4a66-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="e4a66-126">Таким образом, CAB должен указывать на объект за пределами пакета (значение CAB-файла не должно начинаться с префикса \# ).</span><span class="sxs-lookup"><span data-stu-id="e4a66-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="e4a66-127">CAB-файл подписанного объекта не указывает на внешние данные.</span><span class="sxs-lookup"><span data-stu-id="e4a66-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="e4a66-128">\[1 \] — имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="e4a66-128">\[1\] is table name.</span></span> <span data-ttu-id="e4a66-129">\[2 \] является ключом в таблице Media.</span><span class="sxs-lookup"><span data-stu-id="e4a66-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="e4a66-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e4a66-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4a66-131">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="e4a66-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



