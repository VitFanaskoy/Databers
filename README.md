# Databers

//
//  BlendModeSelectorView.swift
//  CollageBuilder
//
//

import SwiftUI

struct BlendModeSelectorView: View {
    
    @Binding var blendMode: ContentBlendMode
    
    var body: some View {
        HStack {
            Text("Blend mode: ")
            Picker("", selection: $blendMode) {
                ForEach(ContentBlendMode.allCases, id: \.self) {
                    Text($0.rawValue)
                }
            }
        }
    }
}

struct BlendModeSelectorView_Previews: PreviewProvider {
    static var previews: some View {
        BlendModeSelectorView(blendMode: .constant(.normal))
    }
}
