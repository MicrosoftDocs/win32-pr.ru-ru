---
title: Код уведомления LVN_GETDISPINFO (Коммктрл. h)
description: Отправляется элементом управления "представление списка" в его родительское окно. Это запрос к родительскому окну для предоставления сведений, необходимых для отображения или сортировки элемента представления списка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804151"
---
# <a name="lvn_getdispinfo-notification-code"></a>\_Код уведомления ЛВН жетдиспинфо

Отправляется элементом управления "представление списка" в его родительское окно. Это запрос к родительскому окну для предоставления сведений, необходимых для отображения или сортировки элемента представления списка. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Во входных данных структура [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , содержащаяся в этой структуре, указывает тип необходимой информации и определяет нужный элемент или подэлемент. Используйте структуру **лвитем** для возврата запрошенной информации в элемент управления. Если обработчик сообщений устанавливает \_ флаг лвиф di \_ сетитем в элементе **Mask** структуры **лвитем** , то элемент управления "представление списка" сохраняет запрашиваемые сведения и больше не запрашивает их.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвдиспинфо**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) . Параметр *wParam* содержит код уведомления.

Элемент управления "представление списка" отправляет код уведомления **ЛВН \_ жетдиспинфо** для получения сведений об элементе, который хранится приложением, а не элементом управления. Сведения могут быть сведениями о тексте или значке для элемента. Это также может быть информация о состоянии элемента. Дополнительные сведения о реализации состояния элемента при обратном вызове см. в сообщении [**LVM \_ сеткаллбаккмаск**](lvm-setcallbackmask.md) .

Дополнительные сведения о обратных вызовах в представлении списка см. [в разделе элементы обратного вызова и маска обратного вызова](list-view-controls-overview.md).

## <a name="examples"></a>Примеры

В следующем примере показано, как можно обработать этот код уведомления, чтобы задать текст в столбцах представления списка. Данные для каждого элемента хранятся в следующей структуре.


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



Ниже приведен \_ обработчик уведомлений WM в процедуре диалогового окна.


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **ЛВН \_ ЖЕТДИСПИНФОВ** (Юникод) и **ЛВН \_ жетдиспинфоа** (ANSI)<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ЛВН \_ сетдиспинфо**](lvn-setdispinfo.md)
</dt> </dl>

 

 





