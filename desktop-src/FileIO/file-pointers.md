---
description: Указатель файла — это 64-разрядное значение смещения, определяющее следующий считанный байт или расположение для получения следующего записанного байта.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Указатели файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263859"
---
# <a name="file-pointers"></a><span data-ttu-id="529f1-103">Указатели файлов</span><span class="sxs-lookup"><span data-stu-id="529f1-103">File Pointers</span></span>

<span data-ttu-id="529f1-104">При открытии файла Windows связывает *указатель файла* с потоком по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="529f1-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="529f1-105">Этот указатель файла является 64-битным значением смещения, которое указывает следующий байт для чтения или расположение для получения следующего записанного байта.</span><span class="sxs-lookup"><span data-stu-id="529f1-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="529f1-106">При каждом открытии файла система помещает указатель файла в начало файла, что является нулевым смещением.</span><span class="sxs-lookup"><span data-stu-id="529f1-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="529f1-107">При каждой операции чтения и записи указатель файла увеличивается на число считанных и записываемых байтов.</span><span class="sxs-lookup"><span data-stu-id="529f1-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="529f1-108">Например, если указатель файла находится в начале файла и запрошена операция чтения 5 байт, то указатель файла будет расположен по смещению 5 сразу после операции чтения.</span><span class="sxs-lookup"><span data-stu-id="529f1-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="529f1-109">По мере чтения или запись каждого байта система перемещает указатель файла.</span><span class="sxs-lookup"><span data-stu-id="529f1-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="529f1-110">Указатель файла можно также переместить, вызвав функцию [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .</span><span class="sxs-lookup"><span data-stu-id="529f1-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="529f1-111">Когда указатель файла достигает конца файла и приложение пытается выполнить чтение из файла, ошибка не возникает, но байты не считываются.</span><span class="sxs-lookup"><span data-stu-id="529f1-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="529f1-112">Поэтому чтение нулевых байтов без ошибки означает, что приложение достиг конца файла.</span><span class="sxs-lookup"><span data-stu-id="529f1-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="529f1-113">При записи нулевых байтов ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="529f1-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="529f1-114">Приложение может усечь или расширить файл с помощью функции [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) .</span><span class="sxs-lookup"><span data-stu-id="529f1-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="529f1-115">Эта функция задает конец файла до текущей позиции указателя файла.</span><span class="sxs-lookup"><span data-stu-id="529f1-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



