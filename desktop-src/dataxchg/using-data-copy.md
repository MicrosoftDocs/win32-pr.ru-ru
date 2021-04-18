---
title: Использование копирования данных
description: В этом разделе приведен пример, демонстрирующий отправку данных между двумя приложениями.
ms.assetid: 5b37aa75-1208-435b-bf81-3e75f48f27f3
keywords:
- Пользовательский интерфейс Windows, копирование данных
- копирование данных, примеры
- копирование данных, WM_COPYDATA сообщение
- Сообщение WM_COPYDATA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e44c4abb9aba68d4db1544f5c7d52220cdc681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700877"
---
# <a name="using-data-copy"></a><span data-ttu-id="05081-107">Использование копирования данных</span><span class="sxs-lookup"><span data-stu-id="05081-107">Using Data Copy</span></span>

<span data-ttu-id="05081-108">В следующем примере показано, как отправить данные между двумя приложениями с помощью сообщения [**WM \_ COPYDATA**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="05081-108">The following example demonstrates how to send information between two applications using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span>

<span data-ttu-id="05081-109">Отправляющее приложение отображает диалоговое окно для пользователя, запрашивающего определенные сведения.</span><span class="sxs-lookup"><span data-stu-id="05081-109">The sending application displays a dialog box to the user which requests certain information.</span></span> <span data-ttu-id="05081-110">Приложение упаковывает информацию в закрытую структуру данных, включает указатель на структуру в структуре [**копидатаструкт**](/windows/win32/api/winuser/ns-winuser-copydatastruct) и отправляет данные принимающему приложению с помощью сообщения [**WM \_ COPYDATA**](wm-copydata.md) .</span><span class="sxs-lookup"><span data-stu-id="05081-110">The application packages the information into a private data structure, includes a pointer to the structure in the [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) structure, and sends the information to the receiving application using the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span> <span data-ttu-id="05081-111">Принимающее приложение имеет скрытое окно с именем класса Disp32Class.</span><span class="sxs-lookup"><span data-stu-id="05081-111">The receiving application has a hidden window with the class name Disp32Class.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
COPYDATASTRUCT MyCDS;
MYREC MyRec;
HRESULT hResult;
BOOL CALLBACK InfoDlgProc( HWND, UINT, WPARAM, LPARAM );
// ************ Code fragment ****************
// Get data from user. InfoDlgProc stores the information in MyRec.
//
   DialogBox( ghInstance, "InfoDlg", hWnd, (DLGPROC) InfoDlgProc );
//
// Copy data into structure to be passed via WM_COPYDATA.
// Also, we assume that truncation of the data is acceptable.
//
   hResult = StringCbCopy( MyRec.s1, sizeof(MyRec.s1), szFirstName );
   if (hResult != S_OK)
        return False;
   hResult = StringCbCopy( MyRec.s2, sizeof(MyRec.s2), szLastName );
   if (hResult != S_OK)
        return False;
   MyRec.n = nAge;
//
// Fill the COPYDATA structure
// 
   MyCDS.dwData = MYPRINT;          // function identifier
   MyCDS.cbData = sizeof( MyRec );  // size of data
   MyCDS.lpData = &MyRec;           // data structure
//
// Call function, passing data in &MyCDS
//
   hwDispatch = FindWindow( "Disp32Class", "Hidden Window" );
   if( hwDispatch != NULL )
      SendMessage( hwDispatch,
                   WM_COPYDATA,
                   (WPARAM)(HWND) hWnd,
                   (LPARAM) (LPVOID) &MyCDS );
   else
      MessageBox( hWnd, "Can't send WM_COPYDATA", "MyApp", MB_OK );
```



<span data-ttu-id="05081-112">Принимающее приложение имеет скрытое окно, которое получает сведения от [**WM \_ COPYDATA**](wm-copydata.md) и отображает его пользователю.</span><span class="sxs-lookup"><span data-stu-id="05081-112">The receiving application has a hidden window which receives the information from [**WM\_COPYDATA**](wm-copydata.md) and displays it to the user.</span></span>


```C++
// ************ Globals ************
//
#define MYDISPLAY 1
typedef struct tagMYREC
{
   char  s1[80];
   char  s2[80];
   DWORD n;
} MYREC;
PCOPYDATASTRUCT pMyCDS;
void WINAPI MyDisplay( LPSTR, LPSTR, DWORD );
//
// ************ Code fragment ****************
//
case WM_COPYDATA:
   pMyCDS = (PCOPYDATASTRUCT) lParam;
   switch( pMyCDS->dwData )
   {
      case MYDISPLAY:
         MyDisplay( (LPSTR) ((MYREC *)(pMyCDS->lpData))->s1,
                    (LPSTR) ((MYREC *)(pMyCDS->lpData))->s2,
                    (DWORD) ((MYREC *)(pMyCDS->lpData))->n );
   }
   break;
```



## <a name="related-topics"></a><span data-ttu-id="05081-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="05081-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="05081-114">**Reference**</span><span class="sxs-lookup"><span data-stu-id="05081-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05081-115">**FindWindow**</span><span class="sxs-lookup"><span data-stu-id="05081-115">**FindWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-findwindowa)
</dt> </dl>

 

 