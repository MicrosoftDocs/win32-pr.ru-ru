---
description: Пример кода, демонстрирующий использование функции сбой getfileattributesex для получения атрибутов файла.
ms.assetid: f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075
title: Получение и изменение атрибутов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2609030d1657b78c266ed6b10841159e0df4d40a2e3b07b0fce42e98b45d54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015142"
---
# <a name="retrieving-and-changing-file-attributes"></a>Получение и изменение атрибутов файлов

Приложение может извлекать атрибуты файла с помощью функции [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) или [**сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) . Функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) и [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) могут задавать многие атрибуты. Однако приложения не могут задавать все атрибуты.

В примере кода в этом разделе Функция [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) используется для копирования всех текстовых файлов (.txt) в текущем каталоге в новый каталог файлов только для чтения. При необходимости файлы в новом каталоге будут изменены на только для чтения.

Приложение создает каталог, указанный в качестве параметра, с помощью функции [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) . Каталог уже не должен существовать.

Приложение ищет в текущем каталоге все текстовые файлы с помощью функций [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) . Каждый текстовый файл копируется в \\ Каталог текстро. После копирования файла функция [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) определяет, доступен ли файл только для чтения. Если файл не только для чтения, приложение изменяет каталоги на \\ текстро и преобразует скопированный файл в только для чтения с помощью функции [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) .

После копирования всех текстовых файлов в текущем каталоге приложение закрывает обработчик поиска с помощью функции [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Константы атрибутов файлов**](file-attribute-constants.md)
</dt> <dt>

[Имена файлов, пути и пространства имен](naming-a-file.md)
</dt> </dl>

 

 



