---
description: При создании устройства в службе "получение образа Windows" (WIA) создается иерархическое дерево элементов WIA, представляющих устройство, а также папки и изображения, связанные с этим устройством.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Перечисление элементов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c216e658b7105f6b3d88d01bd55a3200af7e45c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264532"
---
# <a name="enumerating-items"></a>Перечисление элементов

При создании устройства в службе "получение образа Windows" (WIA) создается иерархическое дерево элементов WIA, представляющих устройство, а также папки и изображения, связанные с этим устройством. Используйте корневой элемент (элемент в корне дерева, представляющий устройство) [**ивиаитем:: енумчилдитемс**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (или [**IWiaItem2:: енумчилдитемс**](-wia-iwiaitem2-enumchilditems.md)), чтобы создать объект перечислителя и получить указатель на его интерфейс [**иенумвиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (или [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)), который используется для навигации по дереву элементов и получения доступа к изображениям или сканирования кроватях, связанных с устройством.

В следующем примере показана функция, которая рекурсивно перечисляет все элементы дерева, начиная с корневого элемента, который передается в функцию.


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



Функция принимает параметр **пвиаитем**, указатель на интерфейс [**Ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (или [**IWiaItem2**](-wia-iwiaitem2.md)) корневого элемента дерева элементов для перечисления.

Во-первых, функция проверяет, является ли элемент папкой или есть ли в нем вложения. Если это так, он вызывает метод [**ивиаитем:: енумчилдитемс**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (или [**IWiaItem2:: енумчилдитемс**](-wia-iwiaitem2-enumchilditems.md)) **пвиаитем** , чтобы создать объект перечислителя для дерева элементов. Если этот вызов выполняется, и перечислитель допустим, функция выполняет итерацию дочерних элементов и рекурсивно вызывает себя для каждого элемента, обрабатывая каждый из них как потенциальный корневой элемент для следующего уровня дочерних элементов.

Таким образом, функция перечисляет все ветви дерева элементов, расположенные ниже корневого элемента, переданного в **енумератеитемс**.

 

 



