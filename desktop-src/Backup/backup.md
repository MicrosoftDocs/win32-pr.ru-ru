---
title: Резервное копирование
description: Разрешите приложениям резервного копирования взаимодействовать с другими приложениями и службами о операциях резервного копирования и восстановления. Выполните резервное копирование ленты, инициализируйте ленту и извлеките сведения о ленточном накопителе. Поддерживать дублирование файлов с помощью хранилища единственных копий (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Резервное копирование резервной копии
- Резервное копирование, Домашняя страница
- Резервное копирование операций восстановления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134230"
---
# <a name="backup"></a><span data-ttu-id="e4705-108">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="e4705-108">Backup</span></span>

<span data-ttu-id="e4705-109">Разделы реестра для резервного копирования и восстановления позволяют приложениям резервного копирования взаимодействовать с другими приложениями и службами о операциях резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="e4705-109">Registry keys for backup and restore allow backup applications to communicate with other applications and services about backup and restore operations.</span></span> <span data-ttu-id="e4705-110">Дополнительные сведения см. в разделах [разделы реестра и значения для резервного копирования и восстановления](registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="e4705-110">For more information, see [Registry Keys and Values for Backup and Restore](registry-keys-for-backup-and-restore.md).</span></span>

<span data-ttu-id="e4705-111">API резервного копирования на ленту позволяет приложениям резервного копирования читать и записывать данные на ленту, инициализировать ленту и получать сведения о ленточных накопителях и ленточных накопителях.</span><span class="sxs-lookup"><span data-stu-id="e4705-111">The tape backup API enables backup applications to read from and write to a tape, initialize a tape, and retrieve tape or tape drive information.</span></span> <span data-ttu-id="e4705-112">Дополнительные сведения см. в статье [резервное копирование на ленту](tape-backup.md).</span><span class="sxs-lookup"><span data-stu-id="e4705-112">For more information, see [Tape Backup](tape-backup.md).</span></span>

<span data-ttu-id="e4705-113">Хранилище единственных копий (SIS) — это архитектура, предназначенная для хранения повторяющихся файлов с минимальными издержками.</span><span class="sxs-lookup"><span data-stu-id="e4705-113">Single-instance store (SIS) is an architecture designed to maintain duplicate files with a minimum of overhead.</span></span> <span data-ttu-id="e4705-114">Приложение резервного копирования использует API резервного копирования SIS для доступа к архитектуре SIS.</span><span class="sxs-lookup"><span data-stu-id="e4705-114">Backup application use the SIS backup API to access the SIS architecture.</span></span> <span data-ttu-id="e4705-115">Дополнительные сведения см. в статье [хранилище единственных копий и резервное копирование SIS](single-instance-store-and-sis-backup.md).</span><span class="sxs-lookup"><span data-stu-id="e4705-115">For more information, see [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).</span></span>

<span data-ttu-id="e4705-116">Резервное копирование и восстановление зашифрованных файлов осуществляется с помощью API необработанного шифрования, который считывает и записывает зашифрованные файлы, сохраняя их в зашифрованном виде.</span><span class="sxs-lookup"><span data-stu-id="e4705-116">Backup and restore of encrypted files is enabled by the raw encryption API, which reads and writes encrypted files while keeping the data in encrypted format.</span></span> <span data-ttu-id="e4705-117">API позволяет выполнять резервное копирование и восстановление зашифрованных данных в этих файлах, в то же время предоставляя цели обеспечения безопасности резервных копий данных и использования приложением, которое не имеет разрешения на использование ключей шифрования в файле.</span><span class="sxs-lookup"><span data-stu-id="e4705-117">The API allows the encrypted data in these files to be backed up and restored, while meeting the goals of maintaining the security of the backed up data, and being usable by an application that lacks permission to use the encryption keys on the file.</span></span> <span data-ttu-id="e4705-118">Дополнительные сведения см. в статье [резервное копирование и восстановление зашифрованных файлов](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span><span class="sxs-lookup"><span data-stu-id="e4705-118">For more information, see [Backup and Restore of Encrypted Files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>

<span data-ttu-id="e4705-119">Средство Срделайед может включать приложения восстановления состояния системы для перемещения, удаления и задания коротких имен системных файлов.</span><span class="sxs-lookup"><span data-stu-id="e4705-119">The Srdelayed tool can enable system state recovery applications to move, delete, and set the short name of system files.</span></span> <span data-ttu-id="e4705-120">Дополнительные сведения см. в разделе [Srdelayed.exe](srdelayed-exe.md).</span><span class="sxs-lookup"><span data-stu-id="e4705-120">For more information, see [Srdelayed.exe](srdelayed-exe.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4705-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e4705-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4705-122">Справочник по резервному копированию</span><span class="sxs-lookup"><span data-stu-id="e4705-122">Backup Reference</span></span>](backup-reference.md)
</dt> </dl>

 

 