---
description: Пример кода, демонстрирующий использование функции сбой getfileattributesex для получения атрибутов файла.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Получение и изменение атрибутов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c980ddd6390f016b2057392f42f6bf645859307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684109"
---
# <a name="retrieving-and-changing-file-attributes"></a><span data-ttu-id="edad6-103">Получение и изменение атрибутов файлов</span><span class="sxs-lookup"><span data-stu-id="edad6-103">Retrieving and Changing File Attributes</span></span>

<span data-ttu-id="edad6-104">Приложение может извлекать атрибуты файла с помощью функции [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) или [**сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) .</span><span class="sxs-lookup"><span data-stu-id="edad6-104">An application can retrieve the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function.</span></span> <span data-ttu-id="edad6-105">Функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) и [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) могут задавать многие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="edad6-105">The [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) functions can set many of the attributes.</span></span> <span data-ttu-id="edad6-106">Однако приложения не могут задавать все атрибуты.</span><span class="sxs-lookup"><span data-stu-id="edad6-106">However, applications cannot set all attributes.</span></span>

<span data-ttu-id="edad6-107">В примере кода в этом разделе Функция [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) используется для копирования всех текстовых файлов (txt) в текущем каталоге в новый каталог файлов только для чтения.</span><span class="sxs-lookup"><span data-stu-id="edad6-107">The code example in this topic uses the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) function to copy all text files (.txt) in the current directory to a new directory of read-only files.</span></span> <span data-ttu-id="edad6-108">При необходимости файлы в новом каталоге будут изменены на только для чтения.</span><span class="sxs-lookup"><span data-stu-id="edad6-108">Files in the new directory are changed to read only, if necessary.</span></span>

<span data-ttu-id="edad6-109">Приложение создает каталог, указанный в качестве параметра, с помощью функции [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="edad6-109">The application creates the directory specified as a parameter by using the [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) function.</span></span> <span data-ttu-id="edad6-110">Каталог уже не должен существовать.</span><span class="sxs-lookup"><span data-stu-id="edad6-110">The directory must not exist already.</span></span>

<span data-ttu-id="edad6-111">Приложение ищет в текущем каталоге все текстовые файлы с помощью функций [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="edad6-111">The application searches the current directory for all text files by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions.</span></span> <span data-ttu-id="edad6-112">Каждый текстовый файл копируется в \\ Каталог текстро.</span><span class="sxs-lookup"><span data-stu-id="edad6-112">Each text file is copied to the \\TextRO directory.</span></span> <span data-ttu-id="edad6-113">После копирования файла функция [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) определяет, доступен ли файл только для чтения.</span><span class="sxs-lookup"><span data-stu-id="edad6-113">After a file is copied, the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function determines whether or not a file is read only.</span></span> <span data-ttu-id="edad6-114">Если файл не только для чтения, приложение изменяет каталоги на \\ текстро и преобразует скопированный файл в только для чтения с помощью функции [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="edad6-114">If the file is not read only, the application changes directories to \\TextRO and converts the copied file to read only by using the [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) function.</span></span>

<span data-ttu-id="edad6-115">После копирования всех текстовых файлов в текущем каталоге приложение закрывает обработчик поиска с помощью функции [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="edad6-115">After all text files in the current directory are copied, the application closes the search handle by using the [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <strsafe.h>

void _tmain(int argc, TCHAR* argv[])
{
   WIN32_FIND_DATA FileData;
   HANDLE          hSearch;
   DWORD           dwAttrs;
   TCHAR           szNewPath[MAX_PATH];   
 
   BOOL            fFinished = FALSE; 

   if(argc != 2)
   {
      _tprintf(TEXT("Usage: %s <dir>\n"), argv[0]);
      return;
   }
 
// Create a new directory. 
 
   if (!CreateDirectory(argv[1], NULL)) 
   { 
      printf("CreateDirectory failed (%d)\n", GetLastError()); 
      return;
   } 
 
// Start searching for text files in the current directory. 
 
   hSearch = FindFirstFile(TEXT("*.txt"), &FileData); 
   if (hSearch == INVALID_HANDLE_VALUE) 
   { 
      printf("No text files found.\n"); 
      return;
   } 
 
// Copy each .TXT file to the new directory 
// and change it to read only, if not already. 
 
   while (!fFinished) 
   { 
      StringCchPrintf(szNewPath, sizeof(szNewPath)/sizeof(szNewPath[0]), TEXT("%s\\%s"), argv[1], FileData.cFileName);

      if (CopyFile(FileData.cFileName, szNewPath, FALSE))
      { 
         dwAttrs = GetFileAttributes(FileData.cFileName); 
         if (dwAttrs==INVALID_FILE_ATTRIBUTES) return; 

         if (!(dwAttrs & FILE_ATTRIBUTE_READONLY)) 
         { 
            SetFileAttributes(szNewPath, 
                dwAttrs | FILE_ATTRIBUTE_READONLY); 
         } 
      } 
      else 
      { 
         printf("Could not copy file.\n"); 
         return;
      } 
 
      if (!FindNextFile(hSearch, &FileData)) 
      {
         if (GetLastError() == ERROR_NO_MORE_FILES) 
         { 
            _tprintf(TEXT("Copied *.txt to %s\n"), argv[1]); 
            fFinished = TRUE; 
         } 
         else 
         { 
            printf("Could not find next file.\n"); 
            return;
         } 
      }
   } 
 
// Close the search handle. 
 
   FindClose(hSearch);
}
```



## <a name="related-topics"></a><span data-ttu-id="edad6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="edad6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edad6-117">**Константы атрибутов файлов**</span><span class="sxs-lookup"><span data-stu-id="edad6-117">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> <dt>

[<span data-ttu-id="edad6-118">Имена файлов, пути и пространства имен</span><span class="sxs-lookup"><span data-stu-id="edad6-118">File Names, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



